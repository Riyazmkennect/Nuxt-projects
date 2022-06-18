<template>
  <div>
    <h1>Grid system</h1>
    <v-container>
      <v-layout row wrap>
        <v-flex xs12 md6>
          <v-btn outlined block class="primary">1</v-btn>
        </v-flex>
        <v-flex xs4 md2>
          <v-btn outlined block class="primary">2</v-btn>
        </v-flex>
        <v-flex xs4 md2>
          <v-btn outlined block class="primary">2</v-btn>
        </v-flex>
        <v-flex xs4 md2>
          <v-btn outlined block class="primary">2</v-btn>
        </v-flex>
      </v-layout>
      <v-layout row wrap justify-space-around>
        <v-flex xs4 md3>
          <v-btn outlined block class="success">Day

😀 </v-btn>
        </v-flex >
         <v-flex xs4 md3>
          <v-btn outlined block class="success">Day

😀 </v-btn>
        </v-flex>
      </v-layout>

       <v-layout row wrap justify-center>
        <v-flex xs4 md3>
          <v-btn outlined block class="yellow">Day

😀 </v-btn>
        </v-flex >
         <v-flex xs4 md3>
          <v-btn outlined block class="yellow">Day

😀 </v-btn>
        </v-flex>
      </v-layout>
       <v-layout row wrap justify-center>
        <v-flex xs4 md3>
          <v-btn outlined block class="success">Day

😀 </v-btn>
        </v-flex >
         <v-flex xs4 md3>
          <v-btn outlined block class="success">Day

😀 </v-btn>
        </v-flex>
      </v-layout>
    </v-container>

    <v-container class="my-5">
      <v-layout row wrap>
         <v-flex xs12  class="elevation-20" height='100%' >
          <v-row  class="justify-center" >
            <v-col cols="10" >
                        <v-btn outlined block class="primary">dubai</v-btn>

            </v-col>
          </v-row>
        </v-flex>

      </v-layout>
    </v-container>
    <v-container>
      
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