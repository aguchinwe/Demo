<template>
   <div>
    <v-app-bar
      class="text px-10"
      dense
      flat
      clipped-left="true"
    > 
       <!-- <v-app-bar-nav-icon></v-app-bar-nav-icon> -->

       <v-toolbar-title><img src="../assets/images/logos-1.png" alt="company-logo"></v-toolbar-title>

      <v-spacer></v-spacer>
      
      <v-btn icon>
        <v-icon class="secondary--text">mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon class="secondary--text">mdi-bell-badge-outline</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon class="secondary--text">mdi-help-circle-outline</v-icon>
      </v-btn>
    </v-app-bar>
     <v-card
    class=""
    width="256"
    flat
  >
    <v-navigation-drawer
      class="secondary"
      flat
      clipped
    >
      <v-list class="py-0">
        <v-list-item >
          <v-list-item-icon>
            <img src="../assets/images/Vector-1.png" alt="dashboard-icon">
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title class="text--text">Dashboard</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </v-card>
   </div>  
</template>
