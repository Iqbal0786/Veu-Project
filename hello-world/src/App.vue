<template>
  <div>
    <img alt="Vue logo" src="./assets/logo.png" />
    <!-- binding text with mustach syntax -->
    <h1>Hii I am {{ name }}</h1>

    <!-- binding text with directive  -->
    <h4 v-text="passion"></h4>

    <h4 >My age is {{ age }}</h4>

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

     <div id="resultDiv">
      Live Output : {{JSON.stringify(formData)}}
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
      }
    };
  },
      methods:{
        postData(){
      alert(JSON.stringify(this.formData))
          console.log(JSON.stringify(this.formData))
        },
        alertAge(){
          console.log(this.age)
        }
      }
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
  width: 70%;
  height: 300px;
  margin: auto;
   text-align: center;
   align-items: center;
   margin-bottom: 20px;
   margin-top: 30px;
   padding: 10px;
   box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
   background-color: #08345b;
   color: white;
}
button{
  padding: 15px 60px;
  background-color: aqua;
  color: black;
  margin-top: 15px;
  border: none;
  border-radius: 20px;
}
#resultDiv{
  width: 70%;
  height: 50px;
  margin: auto;
  margin-top: 40px;
  padding:20px;
  border: 1px solid red;
   background-color: #e42134;
   color: white;
   margin-bottom: 40px;
   font-family: 'Courier New', Courier, monospace;
  box-shadow: rgba(0, 0, 0, 0.25) 0px 14px 28px, rgba(0, 0, 0, 0.22) 0px 10px 10px;
}
</style>
