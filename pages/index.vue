<template>
  <div class="home">
    <div class="face"><Facebook /></div>
    <div class="login"><Login /><p>Create a Page <span>for a celebrity, brand or business.</span> </p></div>
  </div>
</template>

<script>
import Login from "../components/Login";
import Facebook from "../components/Facebook";
export default {
  name: "IndexPage",
  components: { Login, Facebook },
};
</script>
<style>
.home {
  display: flex;
  background-color: #f0f2f5;
}
body {
  background-color: #f0f2f5;
}
.face {
  width: 55%;
  margin: 250px 0 0 auto;
}
.login {
  width: 30%;
  background-color: #f0f2f5;
  margin: 180px 11.5% auto 0;
  border-radius: 5px;
  display: flex;
  flex-direction:column;
  justify-content: center;
  align-items:center;
}
.login p{
  font-weight:bolder;
  margin-top: 20px;
  margin-right: 11.5%;
  font-family: SFProText-Regular, Helvetica, Arial, sans-serif;
}
.login p span{
  font-weight:normal;
  font-family: SFProText-Regular, Helvetica, Arial, sans-serif;
}
.v-application--wrap {
  min-height: 42vh !important;
}
</style>
