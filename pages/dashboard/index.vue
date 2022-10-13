<template>
 <div> 
         <Bars/>
         <main class="dashboard-body">
        <dashboardHeader />
        <v-row class="py-3">
            <v-col cols="12" sm="6" md="4">
                <v-card
                color="#f8f8f8"
                flat
                to="/dashboard/usercreation" 
                >
                    <!-- fill-height -->
                    <!-- <v-row class="" no-gutters> -->
                <v-col cols="12" class="d-flex align-center" px-1>
                   <img src="@/assets/images/todo-icon.png" alt="todo-icon" width="50" height="50">
                    <span class="text-subtitle-1 font-weight-bold secondary--text ml-3">User Creation</span>
                </v-col>
                <!-- </v-row> -->
                </v-card>
            </v-col>
            <v-col cols="12" sm="6" md="4">
                <v-card
                color="#f8f8f8"
                flat
                to="/dashboard/userlist">
                    <!-- <v-row class="fill-height" no-gutters> -->
                <v-col cols="12" class="d-flex align-center" px-1>
                   <img src="@/assets/images/icon-park_log.png" alt="todo-icon" width="50" height="50">
                    <span class="text-subtitle-1 font-weight-bold secondary--text ml-3">User List</span>
                </v-col>
                <!-- </v-row> -->
                </v-card>
            </v-col>
        </v-row> 
        </main>
     </div>
</template>



<script>
export default {

}
</script>

<style>
.dashboard-body{
    position: relative;
    left: 300px;
    bottom: 50px;
}
/* .user-detail{
    position: absolute;
    left: 300px;
    top: 50px;
} */

</style>
