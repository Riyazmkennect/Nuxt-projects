<template>
  <nav>
    <v-toolbar flat app>
      <v-toolbar-side-icon class="white--text"> </v-toolbar-side-icon>

      <v-toolbar-title class="text-uppercase grey--text">
        <span class="font-weight-light">App</span>
        <span>Delhi</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn flat color="blue">
        <span>SIGN OUT</span>
        <!-- <v-icon right>exit_to_app</v-icon> -->

      </v-btn>
    </v-toolbar>
    <v-container class="my-5">
      <v-layout row wrap>
        <v-flex xs12 md4 ms6 lg-3 v-for="person in Team" :key="person.name">
          <v-card flat class="text-center ma-3">
            <v-responsive class="pt-4"> 
              <v-avatar size="100 " class="blue lighten-2">
             <img :src="person.avatar" alt="">
              </v-avatar>
            </v-responsive>
            <v-card-text>
              <div class="subheading">{{ person.name }}</div>
              <div class="grey--text">{{ person.role }}</div>
            </v-card-text>
            <v-card-actions>
              <v-btn flat color="blue ">
               <v-icon small left></v-icon>
               <span>Message</span>
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
    <!-- <v-navigation-drawer v-model="drawer" app class="indigo">
 <v-list>
  <v-list-title>
    <v-list-title-action>
      <v-icon>Dashboard</v-icon>
    </v-list-title-action>
    <v-list-title-content>
      <v-list-title-title>Dashboard</v-list-title-title>
    </v-list-title-content>
  </v-list-title>
 </v-list>
 </v-navigation-drawer> -->
  </nav>
</template>

<script>
export default {
  name: "InspirePage",
  data() {
    return {
      Team: [
        { name: "Syed Riyaz", role: "Software engineer" , avatar:'/avatar-1.png'},
        { name: "Sharukh khan", role: "actor" ,avatar:'/avatar-2.png'},
        { name: "amir khan", role: "actor", avatar:'/avatar-3.png' },
        { name: "Salman khan", role: "actor" , avatar:'/avatar-4.png' },
      ],
    };
  },
};
</script>
