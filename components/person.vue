<template>
<v-container>
    <div id="component-pro" class="d-flex flex-column justify-center align-center">
<img src="~assets/image/Riyaz.jpeg" alt="">   
<h1>{{name}}</h1>
<p>{{description}}</p>
   

    <div id="div" class="d-flex">
    <a href="syedriyaz598@gmail.com" target="_blank"> <v-icon dark>mail</v-icon></a>
    <a href="https://www.youtube.com/watch?v=3lNLG8DBLQQ" target="_blank"> <v-icon dark>person</v-icon></a>
    <a href="https://www.youtube.com/watch?v=ltzlhAxJr74" target="_blank"> <v-icon dark>Linkedln</v-icon></a>
    </div>


    </div>
</v-container>
</template>
<script>
export default {
    data(){
      return {
        name:"Syed Riyaz",
        description:"Iam software engineer "
      }
    }
    
}
</script>

<style scoped lang="scss">
#component-pro{
    height:100vh;
    img{
        max-height: 100px;
        border-radius: 100px;
    }
}
#div{
    align-content: center;
}
</style>
