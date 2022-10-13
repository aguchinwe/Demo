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
                    :items="items"
                    :required="true"></v-select>
                    <v-text-field
                     label="Middle name"
                     solo outlined flat dense
          ></v-text-field>
          <v-text-field
                     label="+234 Phone number"
                     solo outlined flat dense
                     :required="true"
          ></v-text-field>
                </v-form>
            </v-col>
            <v-col cols="4">
                <v-text-field
                     label="First name"
                     solo outlined flat dense
                     :required="true"
          ></v-text-field>
          <v-text-field
                     label="Last name"
                     solo outlined flat dense
                     :required="true"
          ></v-text-field>
          <v-text-field
                     label="Email address"
                     solo outlined flat dense
                     :required="true"
          ></v-text-field>
            </v-col>
          
        </v-row>
         <div class="d-flex align-center but"> <v-btn class="rounded primary text--text" block>Done</v-btn></div>  
        </main>
    </div>
</template>

<script>
export default {
data: () => ({
    items: ['Mr', 'Mrs', 'Miss', 'Master']
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
