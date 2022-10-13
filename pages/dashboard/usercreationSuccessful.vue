<template>
    <div >
        <Bars />
        <main class="dashboard-body">
        <dashboardHeader/>
        <p class="text-subtitle-2 primary--text py-2">User Creation</p>
        <v-row class="py-2">
            <v-col cols="4">
                <v-form ref="form"
             v-model="valid"
             lazy-validation>
                    <v-select
                    label="Title"
                    solo outlined flat dense
                    :items="items"></v-select>
                    <v-text-field
                     label="Middle name"
                     solo outlined flat dense
          ></v-text-field>
          <v-text-field
                     label="+234 Phone number"
                     solo outlined flat dense
          ></v-text-field>
                </v-form>
            </v-col>
            <v-col cols="4">
                <v-text-field
                     label="First name"
                     solo outlined flat dense
          ></v-text-field>
          <v-text-field
                     label="Last name"
                     solo outlined flat dense
          ></v-text-field>
          <v-text-field
                     label="Email address"
                     solo outlined flat dense
          ></v-text-field>
            </v-col>
          
        </v-row>
         <div class="d-flex align-center but"> <v-btn class="rounded primary text--text" block>Done</v-btn></div>  
        </main>
        <v-overlay :value="overlay" :opacity="opacity">
            <v-card class="rounded-xl">
            <v-list color="text" width="300"
         height="170">
        <v-list-item  
        class="d-flex flex-column"
         color="text">
          <v-list-item-content class="pb-0">
            <div class="secondary--text">User Creation</div>
          </v-list-item-content>

          <v-list-item-content class="pt-0">
            <v-list-item-title class="secondary--text text-h4 font-weight-bold">Successful</v-list-item-title>
          </v-list-item-content>

          <!-- <v-list-item-icon> -->
            <v-btn class="" 
            elevation="0"
            color="text">
            <img src="@/assets/images/Vectorgood.png" alt="good-icon" width="60" height="60">
        <!-- <v-icon class="secondary--text">mdi-checkbox-marked-circle</v-icon> -->
      </v-btn>
            
          <!-- </v-list-item-icon> -->
        </v-list-item>
      </v-list>
            </v-card>
        </v-overlay>
    </div>
</template>

<script>
export default {
data: () => ({
    items: ['Mr', 'Mrs', 'Miss', 'Master'],
    overlay: true,
    opacity: 0.8,
    
})
}
</script>

<style>
.dashboard-body{
    position: relative;
    left: 300px;
    bottom: 50px;
}
.but{
     width: 300px;
     position: relative;
     left: 300px; 
}

</style>
