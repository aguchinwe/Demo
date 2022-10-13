<template>
  <div>
       <v-row class="ro">
        <v-container fluid class="d-flex d-flex-row b">
         <v-col class="col-lg-8 info">
            <img src="..\assets\images\login.png" alt="login-image" width="440" height="260" class="img">
        </v-col>
        <v-col class="col-lg-4">
          <v-container> 
            <div class="d-flex flex-column align-center justify-content-center">
              <img src="..\assets\images\logos-1.png" alt="company-logo">
             <v-form ref="form"
             v-model="valid"
             lazy-validation
             >
              <v-text-field
            label="Username"
            solo outlined flat dense
          ></v-text-field>
          <v-text-field
            label="Password"
            solo outlined flat dense
          ></v-text-field>
<v-btn class="rounded primary text--text" block >LOGIN</v-btn>
<!-- v-click.prevent="favour()" -->
          <p class="accent--text body-2 font-weight-light mt-4 mb-0">Don't have an account?<span class="secondary--text font-weight-bold">Create</span></p>
          <p class="secondary--text body-2 text-center">Forgot Password?</p>
             </v-form>
           </div>
            </v-container>
            
        </v-col>
        </v-container>
       
    </v-row>
    <div class="col-10 col-sm-8 mx-auto">
     
    </div>
  </div>
</template>

<script>
// import { DEFAULT_RULE } from "@/constants/";
export default {
//   components: {},
//   layout: "ActionPage",
//   middleware: "guest",
  data: () => ({
    dialog: true,
    valid: false,
    login: {
      usernameEmailPhoneNumber: "",
      password: "",
      restriction: "State",
    },
  }),
 
//   computed: {
//     rule() {
//       return DEFAULT_RULE;
//     },
//   },
//   methods: {
//     async signIn() {
//       if (this.$refs.form.validate()) {
//         await this.$store.dispatch("staff/login", this.login);
//       }
//     },
//   },
};
</script>
<style scoped>
.ro{
  /* border: solid 1px black; */
  height: 600px;
}
.img{
  position: relative;
  left: 150px;
  top: 150px;
}

</style>
