<template lang="">
    <div>
         <img class="logo" src="../assets/logo.jpg"/>
        <h1>Sign up</h1>
        
    </div>

    <div class="register">
        <input type="text" class="" placeholder="Name"/>
        <input type="email" class="" placeholder="Email"/>
        <input type="password" class="" placeholder="Password"/>
        <button>Sign Up</button>

    </div>
   
</template>

<script>
export default {
  name: "SignUp",
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
  border:1px solid skyblue;
}

.register button {
  width: 320px;
  height: 40px;
  background: skyblue;
  color: white;
  cursor: pointer;
  border:1px solid skyblue;
}
</style>
