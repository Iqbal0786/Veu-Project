<template>
  <img alt="Vue logo" src="./assets/logo.png">
   <div>Hii {{name}}</div>
</template>

<script>


export default {
  name: 'App',
    data(){
      return {name:"Iqbal"}
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
