<template>
    <div>
        <v-row>
            <v-col cols="12" class="d-flex justify-center display-2">
                <div class="d-flex justify-center">
                    ezTrack Staff Location Check In
                </div>
            </v-col>
        </v-row>
        <v-row class="mt-4">
            <v-col cols="7">
                <div class="headline">
                    ezTrack helps staff in your organization check in their locations easily
                    <br /><br />
                    Add key locations in your organization premise and generate Area based or Location Specific QR codes right from ezTrack dashboard
                    <br /><Br />
                    Staff just scan the QR code using their phones to check in to the location
                    <br />
                </div>
            </v-col>

            <v-col cols="1">
                <v-divider
                vertical
                light
                ></v-divider>
            </v-col>

            <v-col cols="4">
                    <div class='title d-flex justify-center'>
                        To get started, <Br />enter your company identifier below <br />(e.g yourcompany.eztrack.cloud)
                    </div>
                    <div class="mt-4">
                        <v-text-field
                            outlined
                            suffix=".eztrack.cloud"
                            v-model="companyid"
                        >
                        </v-text-field>
                    </div>
                    <div class="d-flex justify-center" v-if="companyexist === true">
                        <v-alert type="error" dense>
                            Company ID {{companyid}} already exist. Please enter another ID.
                        </v-alert>
                    </div>
                    <div class="d-flex justify-end">
                        <v-btn color="primary" @click='createcompany'>Create</v-btn>
                    </div>
                    
            </v-col>
        </v-row>
    </div>
</template>

<script>
const baseURI = "http://localhost:3000/";

export default {
    name: 'MainLanding',
    data:() => ({
        companyid: null,
        companyexist: false,
    }),
    methods: {
        createcompany: function(){
            var self = this;

            this.$http.get(baseURI + 'company/checkifcompanyexist',{
                params:{
                    cid: this.companyid
                }
            }).then(function(response){
               
                if (response.status === 200){
                    let data = response.data;

                    if (data === 'true'){
                        self.companyexist = true;
                    }
                    else if(data === 'false'){
                        self.companyexist = false;
                    }
                }
                else if(response.status === 400){
                    alert('An error has occured. Err ' + response.data);
                }
            });
        }
    },
}
</script>

<style scoped>

</style>