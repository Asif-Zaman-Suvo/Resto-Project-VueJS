<template lang="">
  <div>
    <img class="logo" src="../assets/logo.jpg" />
    <h1>Sign up</h1>
  </div>

  <div class="register">
    <input type="text" v-model="name" class="" placeholder="Name" />
    <input type="email" v-model="email" class="" placeholder="Email" />
    <input type="password" v-model="password" class="" placeholder="Password" />
    <button v-on:click="signUp">Sign Up</button>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "SignUp",
  data() {
    return {
      name: "",
      email: "",
      password: "",
    };
  },
  methods: {
    async signUp() {
      let result = await axios.post("http://localhost:3000/users", {
        email: this.email,
        name: this.name,
        password: this.password,
      });

      console.log(result);
      if (result.status == 201) {
        alert("sign up done");
        localStorage.setItem("User-Info", JSON.stringify(result.data));
        this.$router.push({name:"Home"})
      }
    },
  },
};
</script>

<style>
.logo {
  width: 100px;
}

.register input {
  width: 300px;
  height: 40px;
  padding-left: 20px;
  display: block;
  margin-bottom: 30px;
  margin-right: auto;
  margin-left: auto;
  border: 1px solid skyblue;
}

.register button {
  width: 320px;
  height: 40px;
  background: skyblue;
  color: white;
  cursor: pointer;
  border: 1px solid skyblue;
}
</style>
