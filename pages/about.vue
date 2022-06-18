<template>
  <div>
      <Navigation/>
    <nav>
        <v-toolbar flat app>
  <v-toolbar-side-icon class="white--text">
 
  </v-toolbar-side-icon>

  <v-toolbar-title class="text-uppercase grey--text">
    <span class="font-weight-light">App</span>
    <span>Delhi</span>
  </v-toolbar-title>
  
  <v-spacer></v-spacer>
  <v-btn flat color="green">
  <span>SIGN OUT</span>
  <!-- <v-icon right>exit_to_app</v-icon> -->
  </v-btn>

 </v-toolbar>
    </nav>
    <v-container class="my-5">
        
      <v-layout row class="mb-3">
        <v-tooltip>
            
        </v-tooltip>
          <v-btn small flat  color="grey" @click="sortBy('title')">
            <v-icon left small>mdi-plus</v-icon>
            <span class="caption text-lowercase"> By project Name</span>
          </v-btn>
           <v-btn small flat  color="grey" @click="sortBy('person')">
            <v-icon left small></v-icon>
            <span class="caption text-lowercase"> By person Name</span>
          </v-btn>
      </v-layout>


      <v-card flat class="pa-3" v-for="project in projects " :key="project.title">
        <v-layout row :class="'pa-3 project ${project.status}'">
          <v-flex xs12 md6>
            <div class="caption blue--text">project Title</div>
            <div>{{project.title}}</div>
          </v-flex>
          <v-flex xs6 md2 sm4>
            <div class="caption blue--text">Person</div>
            <div>{{project.person}}</div>
          </v-flex>
          <v-flex xs6 md2 sm4>
            <div class="caption blue--text">Due by</div>
            <div>{{project.due}}</div>
          </v-flex>
          <v-flex xs6 md2 sm4>
            <div class="right">
                <v-chip small :class="'${project.status} orange--text caption my-2'">{{project.status}}</v-chip>
            </div>
          </v-flex>
       
        </v-layout>
        <v-divider></v-divider>
      </v-card>
    </v-container>
  </div>
</template>
<script>
import Navigation from '../components/Navigation.vue';
export default {
  components:{
    Navigation
  },
  data() {
    return {
      projects: [
        {
          title: "design a website",
          person: "Syed Riyaz",
          due: "1 jun",
          status: "ongoing",
          content:'lorem'
        },
        {
          title: "design a dashboard",
          person: "Syed Riyaz",
          due: "7 jun",
          status: "complete",
           content:'lorem'
        },
        {
          title: "design ui",
          person: " Riyaz",
          due: "10 jun",
          status: "ongoing",
           content:'lorem'
        },
        {
          title: "design thank you page",
          person: " Riyaz",
          due: "4 jun",
          status: "complete",
           content:'lorem'
        },
      ],
    };
   
  },
   methods:{
    sortBy(prop){
        this.projects.sort((a,b)=> a[prop] < b[prop]? -1 : 1 )
    }
        
    }


};
</script>
<style>
.project.completed{
    border-left: 4px solid  orange;
}
.project.ongoing{
    border-left: 4px solid  rgb(0, 89, 255);
}
.project.onSite{
    border-left: 4px solid  rgb(179, 255, 0);
}
.v-chip.complete{
    background:greenyellow ;
}
.v-chip.ongoing{
    background:rgb(47, 224, 255) ;
}
.v-chip.onSite{
    background:greenyellow ;
}
</style>