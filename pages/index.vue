<template>

 <nav>
 <v-toolbar flat app>
  <v-toolbar-side-icon class="white--text">

  </v-toolbar-side-icon>

  <v-toolbar-title class="text-uppercase grey--text">
    <span class="font-weight-light">App</span>
    <span>Delhi</span>
    
  </v-toolbar-title>
  
  <v-spacer></v-spacer>

  <v-menu offset-y>
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          color="primary"
          dark
          v-bind="attrs"
          v-on="on"
        >
          Dropdown
        </v-btn>
      </template>
      <v-list>
        <v-list-item
          v-for="(item, index) in items"
          :key="index"
        >
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>

    <v-menu>
    <v-btn flat slot="activator" color="grey"> <v-icon> </v-icon>
    <span>Menu</span>
    </v-btn>
    <v-list>
    <v-list-title v-for="link in links" :key="link.text" router :to="link.route">
    <v-list-title-title>
    {{link.text}}
    </v-list-title-title>
    </v-list-title>
    </v-list>
    </v-menu>
    

  <v-btn flat color="green">
  <span>SIGN OUT</span>
  </v-btn>
 </v-toolbar>
 <h1 class="mx-4 mt-3">Dubai</h1>
 <v-container class="my-5">
<p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Minus dolore commodi beatae ab harum 
  dignissimos ea quia sunt soluta facere dolor
   aliquid odit quod impedit aut libero nam, ratione maiores.</p>

   <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Nemo voluptas molestias nulla eveniet, autem maxime harum, sequi dolore minima quo nesciunt natus animi
     perferendis non dolores cupiditate? Aspernatur, tempora! Aliquam.</p>
 </v-container>
  <div>
        <v-container class="my-5">
      <v-card flat class="pa-3">
        <v-layout row wrap>
          <v-flex xs12 md6>
            <div class="caption blue--text">project Title</div>
            <div>Create a new website</div>
          </v-flex>
          <v-flex xs6 md2 sm4>
            <div class="caption blue--text">Person</div>
          </v-flex>
        </v-layout>
      </v-card>
    </v-container>
    </div>
 
 </nav>
 
</template>

<script>
export default {
  name: 'IndexPage',
  data(){
    return {
      drawer:false
    }
  }
}
</script>
