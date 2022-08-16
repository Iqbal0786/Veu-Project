<template>
  <div>
    <img alt="Vue logo" src="./assets/logo.png" />
    <!-- binding text with mustach syntax -->
    <div>Hii I am {{ name }}</div>

    <!-- binding text with directive  -->
    <div v-text="passion"></div>

    <div>My age is {{ age }}</div>

    <div id="formData">
      <h1>Register from here</h1>
      <form @submit.prevent="postData">
        <label for="name">Name : </label>
        <input type="text" placeholder="name" v-model="formData.name" /><br />
        <label for="email">Email : </label>
        <input
          type="email"
          placeholder="email address"
          v-model="formData.email"
        /><br />
        <label for="password">Password : </label>
        <input
          type="password"
          placeholder="password"
          v-model="formData.password"
        /><br />
        <label for="skill">Select Skills : </label>
        <input type="checkbox" value="Node.js" v-model="formData.skills" />
        <label for="">Node.js</label>
        <input type="checkbox" value="ReactJs" v-model="formData.skills" />
        <label for="">ReactJs</label>
        <input type="checkbox" value="MongoDb" v-model="formData.skills" />
        <label for="">MongoDb</label>
        <input type="checkbox" value="Express" v-model="formData.skills" />
        <label for="">Express</label><br>
        <button >Submit</button>
      </form>
    </div>

     <div>
       out put : {{JSON.stringify(formData)}}
     </div>
    <!-- root end -->
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      name: "Iqbal",
      passion: " I am a Full Stack Web Developer ",
      age: 21,
      formData: {
        name: "",
        email: "",
        password: "",
        skills: [],
      },
      methods:{
        postData(){
          alert("Hii")
          //event.preventDefault();
     
          console.log(this.formData)
        }
      }
    };
  },
};
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
label{
  font-family: 'Courier New', Courier, monospace;
  
}
input{
  margin-bottom: 10px;
  margin-left: 20px;
}
#formData{
   text-align: center;
   align-items: center;
   margin-bottom: 20px;
}
button{
  padding: 15px 60px;
  background-color: aqua;
  color: black;
  margin-top: 15px;
  border: none;
  border-radius: 20px;
}
</style>
