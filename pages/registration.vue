<template>
     <!-- <div> -->
       <v-row class="fill-height">
        <!-- <v-container fluid class="d-flex d-flex-row"> -->
         <v-col cols="12" md="7" class="d-none d-md-block pa-0 info">
             <div class="fill-height d-flex justify-center align-center info">
             <img src="..\assets\images\reg.png" alt="login-image" width="55%" >
             </div>
        </v-col>
        <v-col class="col-lg-5">
            <div class="d-flex flex-column align-center justify-content-center">  
             <img src="..\assets\images\logos-1.png" alt="company-logo" width="80px" class="mt-5 mb-2">
             <p class="font-weight-bold text-center secondary--text">Create <span class="secondary--text font-weight-thin">Account</span></p>
             <div class="col-10 col-sm-8 mx-auto">
             <v-form ref="form"
             v-model="valid"
             lazy-validation
             >
              <v-text-field
            label="Username"
            required
            v-model="username"
            solo outlined flat dense
          ></v-text-field>
          <!-- <v-text-field
            label="Phone number"
            solo outlined flat dense
          ></v-text-field> -->
          <v-text-field
            label="Email"
            v-model="email"
            :rules="emailRules"
            required
            solo 
            outlined 
            flat 
            dense
          ></v-text-field>
          <v-text-field
            label="Password"
            :rules="passwordRules"
            required
            type="password"
            v-model="password"
            solo outlined flat dense
          ></v-text-field>
          <!-- <v-text-field
            label="Re-enter password"
            solo outlined flat dense
          ></v-text-field> -->
            <v-btn class="rounded primary text--text" block v-on:click.prevent="register()">Submit</v-btn>
            <div class="subtitle-1 text-center pt-5 accent--text">
          <!-- <p class="accent--text body-2 font-weight-light mt-4 mb-0"> -->
            Already have an account?
            <span class="secondary--text font-weight-bold">
              sign in
              </span>
            <!-- </p> -->
        </div>
             </v-form>
             </div>
             </div>   
             <!-- </v-container> -->
            </v-col>  
        <!-- </v-container> -->
    </v-row>
    <!-- </div> -->
</template>

<script>
export default {
  data() { 
    username:''
    email:''
    password:''
    // emailRules: v => !!v || 'Email is required'
    emailRules: [ 
    v => !!v || 'Email is required', 
    v => /.+@.+/.test(v) || 'E-mail must be valid' 
]
// email: '',
//       emailRules: [
//         v => !!v || 'E-mail is required',
//         v => /.+@.+\..+/.test(v) || 'E-mail must be valid',
//       ]
// passwordRules: [v => !!v || 'Password is required']
passwordRules: [ 
    v => !!v || 'Password is required', 
    v => (v && v.length >= 5) || 'Password must have 5+ characters',
    v => /(?=.*[A-Z])/.test(v) || 'Must have one uppercase character', 
    v => /(?=.*\d)/.test(v) || 'Must have one number', 
    v => /([!@$%])/.test(v) || 'Must have one special character [!@#$%]' 
]
    return { 
      username:"", 
      password:"" ,
      email: "", 
    };
    
    },
  methods:{
    register(){
      console.log(this.username);
      console.log(this.email);
      console.log(this.password);
      var axios = require('axios');
var data = JSON.stringify({
  "name": this.username,
  "email": this.email,
  "password": this.password,
});

var config = {
  method: 'post',
  url: 'https://api.backendless.com/E84B7960-BBF3-6736-FF54-2E33BEDEBE00/FB8C2B7D-9F89-4E8E-B723-ACA311A40C1C/users/register',
  headers: { 
    'Content-Type': 'application/json'
  },
  data : data
};

axios(config)
.then(function (response) {
  //
  console.log(JSON.stringify(response.data));
  //redirect to dash board which will check for a cookies before allowing access to its content
  window.location.href = "/login";
})
.catch(function (error) {
  console.log(error);
});
    },
  },
}
</script>

<style scoped>
/* .img{
  position: relative;
  left: 150px;
  top: 150px;
} */
</style>

