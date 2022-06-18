<template>
    <div>
        <h1>{{output()}}</h1>
        <p>learn more <a v-bind=" congratulations" href="link"> congratulations</a> as </p>
       <p>{{output()}}</p>
       <button v-on:click="add()">add</button>
       <button v-on:click="remo()">remo</button>
       <p>{{counter}}</p>
       <input type="text" v-on:click="setName">
       <p>{{name}}</p>
    </div>
</template>
<script>
export default {
    name:'basic',
    data(){
        return{
            // coarse:'developer',
            // link:'https://www.udemy.com/course/vuejs-2-the-complete-guide/learn/lecture/21463140#overview',
            // lam:'developer',
            counter:0,
            name:''
        }
    },
    methods:{
        setName(e){
          this.name=event.target.value
        },
      output(){
        const randomNumber=Math.random();
            if(randomNumber < 0.1){
              return 'developer'
            }else{
                return this.lam
            }
        
      },
      add(){
        this.counter=this.counter + 1;
      },
      remo(){
        this.counter=this.counter-1
      }
    }
}
</script>