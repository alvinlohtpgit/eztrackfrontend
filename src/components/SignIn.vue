<template>
    <div>
        <v-row>
            <v-col cols="6">
                <div class="headline">Create a new acount</div>

                 <v-container class="mt-8">
                     <v-row no-gutters>
                         <v-col cols="3">
                            Email
                         </v-col>
                         <v-col cols="8">
                             <v-text-field v-model='signup_email' filled dense label='You will use this email to sign in to ezTrack'></v-text-field>
                         </v-col>
                     </v-row>

                     <v-row no-gutters>
                         <v-col cols="3">
                            First Name
                         </v-col>
                         <v-col cols="8">
                             <v-text-field v-model='signup_firstname' filled dense></v-text-field>
                         </v-col>
                     </v-row>

                     <v-row no-gutters>
                         <v-col cols="3">
                            Last Name
                         </v-col>
                         <v-col cols="8">
                             <v-text-field v-model='signup_lastname' filled dense></v-text-field>
                         </v-col>
                     </v-row>


                     <v-row no-gutters>
                         <v-col cols="3">
                            Password
                         </v-col>
                         <v-col cols="8">
                             <v-text-field v-model='signup_password1' filled dense></v-text-field>
                         </v-col>
                     </v-row>

                     <v-row no-gutters>
                         <v-col cols="3">
                            Password Again
                         </v-col>
                         <v-col cols="8">
                             <v-text-field v-model='signup_password2' filled dense></v-text-field>
                         </v-col>
                     </v-row>

                      <v-row no-gutters>
                         <v-col cols="11">
                             <div class="d-flex justify-end">
                                 <v-btn color="primary" @click='dosignup'>Sign Up</v-btn>
                             </div>
                         </v-col>
                     </v-row>

                 </v-container>
            </v-col>

            <v-col cols="1">
                <v-divider vertical light></v-divider>
            </v-col>

            <v-col cols="5">
                <div class="headline">Already have an account? Sign In</div>
                <v-container class="mt-8">
                    <v-row no-gutters>
                        <v-col cols="3">
                            Email
                        </v-col>
                        <v-col cols="8">
                            <v-text-field filled dense></v-text-field>
                        </v-col>
                    </v-row>

                    <v-row no-gutters>
                        <v-col cols="3">
                            Password
                        </v-col>
                        <v-col cols="8">
                            <v-text-field filled dense></v-text-field>
                        </v-col>
                    </v-row>

                    <v-row no-gutters>
                        <v-col cols="11">
                            <div class="d-flex justify-end">
                                <v-btn color="primary">Login</v-btn>
                            </div>
                        </v-col>
                    </v-row>
                </v-container>
            </v-col>
        </v-row>
    </div>    
</template>

<script>
export default {
    name: 'SignIn',
    data: () => ({
        signup_email: null,
        signup_password1: null,
        signup_password2: null,
        signup_firstname: null,
        signup_lastname: null,
        email_already_exist: false,
    }),
    methods:{
        dosignup: function(){
            // Check that the email doesn't exist 
           // alert(process.env.VUE_APP_SERVERPATH);
           
        }
    }
}
</script>

<style scoped>

</style>