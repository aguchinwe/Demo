<template>
    <div>
        <Bars/>
        <main class="dashboard-body">
             <p class="text-subtitle-1 font-weight-bold primary--text ml-3">User <span class="secondary--text font-weight-thin">List</span></p>
             
                <v-data-table
                    :headers="headers"
                    :items="details"
                   hide-default-footer
                    class="elevation-0"
                ></v-data-table>
 <!-- :items-per-page="5" -->
                 <div class="d-flex align-center but"> <v-btn class="rounded primary text--text" block>UPLOAD</v-btn></div>
        </main>
    </div>
</template>

<script>
export default {
    data () {
      return {
        headers: [
          {
            text: 'Title',
            align: 'start',
            // sortable: false,
            value: 'title',
            class: 'secondary--text',
          },
          { text: 'First Name', value: 'firstname', class: 'secondary--text',},
          { text: 'Middle Name', value: 'middlename', class: 'secondary--text', },
          { text: 'Last Name', value: 'lastname', class: 'secondary--text', },
          { text: 'Email', value: 'email', class: 'secondary--text', },
        ],
        details: [
          {
            title: 'Mr',
            firstname: 'Miles',
            middlename: 'Gonzalo',
            lastname: 'Morales',
            email: 'blank',
          },
           {
            title: 'Mrs',
            firstname: 'Gwen',
            middlename: 'Maxine',
            lastname: 'Stacey',
            email: 'blank',
          },
           {
            title: 'Mr',
            firstname: 'Miles',
            middlename: 'Gonzalo',
            lastname: 'Morales',
            email: 'blank',
          },
        ],
      }
    },

}
</script>

<style>
.dashboard-body{
    position: relative;
    left: 300px;
    bottom: 50px;
    width: 60%;
}
tbody tr:nth-of-type(odd) {
   background-color: rgba(0, 0, 0, .05);
 }
 .but{
     width: 250px;
     position: relative;
     left: 250px;
     top: 50px; 
}
</style>
