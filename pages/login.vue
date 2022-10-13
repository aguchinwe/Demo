<template>
  <!-- <div> -->
       <v-row class="fill-height">
        <!-- <v-container fluid class="d-flex d-flex-row b"> -->
         <v-col col="12" md="7" class="d-none d-md-block pa-0 info">
           <div class="fill-height d-flex justify-center align-center info">
            <img src="..\assets\images\login.png" alt="login-image" width="55%">
        </div>
        </v-col>
        <v-col class="col-lg-5">
          <!-- <v-container>  -->
            <div class="d-flex flex-column align-center justify-content-center">
              <img src="..\assets\images\logos-1.png" alt="company-logo"
              width="80px" class="mt-15 mb-2">
                <div class="col-10 col-sm-8 mx-auto">
             <v-form ref="form"
             v-model="valid"
             lazy-validation
             >
              <v-text-field
            label="Username"
            v-model="username"
            required
            :rules="[v => !!v || 'Username is required']"
            solo 
            outlined 
            flat 
            dense
          ></v-text-field>
          <v-text-field
            label="Password"
            v-model="password"
            type="password"
            :rules="[v => !!v || 'Password is required']"
            required
            solo 
            outlined 
            flat 
            dense
          ></v-text-field>
          <nuxt-link to="/dashboard">
          <v-btn class="rounded primary text--text" block >LOGIN</v-btn></nuxt-link>
          <div class="subtitle-1 text-center pt-5">
          <!-- <p class="accent--text body-2 font-weight-light mt-4 mb-0"> -->
            Don't have an account?
            <span class="secondary--text font-weight-bold">Create</span>
            <!-- </p> -->
          <p class="secondary--text body-2 text-center">Forgot Password?</p>
          </div>
          <!-- <div class="subtitle-1 text-center pt-5">
            <span>Already have an account?</span>
            <nuxt-link to="/login" class="primary--text font-weight-bold">
              Go to login
            </nuxt-link>
          </div> -->
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
  data: () => ({
    username: null,
    password: null,
    
    // dialog: true,
    // valid: false,
    // login: {
    //   usernameEmailPhoneNumber: "",
    //   password: "",
    //   restriction: "State",
    // },
  }),
 
};
</script>
<style scoped>
/* .ro{
  border: solid 1px black;
  height: 600px;
} */
.img{
  position: relative;
  left: 150px;
  top: 150px;
}

</style>


<script>

</script>
