<template>
<!-- <v-container>
  <h1 class="ml-12">typography</h1>
  <v-card>
    <v-card-text>
        <h1 class="purple">header</h1>
         <input type="text">
         <button>click</button>
    </v-card-text>
  </v-card>
  </v-container> -->
   <!-- <v-card
    class="d-flex "
    outlined
    tile
    
  >
    <div class="d-flex justify-space-around">
      
      <img  src="~assets/image/Riyaz.jpeg"/>
      <v-card-text class="">
        <h2>Syed Riyaz</h2>
      </v-card-text>
      
    </div>
  </v-card> -->
 <v-container>
    <!-- <v-card
        v-for="n in 40"
        :key="n"
        class="pa-2"
        outlined
        tile
      >
        <img  src="~assets/image/Riyaz.jpeg"/>
      </v-card> -->
      <template>
  <div>
    <v-card
      class="d-flex justify-start mb-6"
      :color="$vuetify.theme.dark ? 'grey darken-3' : 'grey lighten-4'"
      flat
      tile
    >
      <!-- <v-card
        v-for="n in 3"
        :key="n"
        class="pa-2"
        outlined
        tile
      >
        justify-start
      </v-card> -->
    </v-card>

    <!-- <v-card
      class="d-flex justify-end mb-6"
      :color="$vuetify.theme.dark ? 'grey darken-3' : 'grey lighten-4'"
      flat
      tile
    >
      <v-card
        v-for="n in 3"
        :key="n"
        class="pa-2"
        outlined
        tile
      >
        justify-end
      </v-card>
    </v-card> -->

    <!-- <v-card
      class="d-flex justify-space-between mb-6"
      :color="$vuetify.theme.dark ? 'grey darken-3' : 'grey lighten-4'"
      flat
      tile
    >
      <v-card
        v-for="n in 4"
        :key="n"
        class="pa-2 "
        outlined
        tile
      >
        <img  src="~assets/image/Riyaz.jpeg"/>
      </v-card>
    </v-card> -->
    <v-card
      class="d-flex justify-space-around mb-6"
     
    >
      <v-card
        v-for="n in 3"
        :key="n"
        class="pa-2"
       
      >
       <img  src="~assets/image/Riyaz.jpeg"/>
      </v-card>
    </v-card>

    <!-- <v-card
      class="d-flex justify-space-between mb-6"
      :color="$vuetify.theme.dark ? 'grey darken-3' : 'grey lighten-4'"
      flat
      tile
    >
      <v-card
        v-for="n in 3"
        :key="n"
        class="pa-2"
        outlined
        tile
      >
        justify-space-between
      </v-card>
    </v-card> -->

    <!-- <v-card
      class="d-flex justify-space-around mb-6"
      :color="$vuetify.theme.dark ? 'grey darken-3' : 'grey lighten-4'"
      flat
      tile
    >
      <v-card
        v-for="n in 3"
        :key="n"
        class="pa-2"
        outlined
        tile
      >
        justify-space-around
      </v-card>
    </v-card> -->
  </div>
</template>
 </v-container>
  

</template>

<script>
export default {

}
</script>

<style>

</style>