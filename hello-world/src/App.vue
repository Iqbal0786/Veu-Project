<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <!-- binding text with mustach syntax -->
   <div>Hii I am  {{name}}</div>  

   <!-- binding text with directive  -->
   <div v-text="passion"></div>

   <div> My age is {{age}}</div>
    
</template>

<script>


export default {
  name: 'App',
    data(){
      return {name:"Iqbal",
        passion:" I am a Full Stack Web Developer ",
        age:21
          
      }
    }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
