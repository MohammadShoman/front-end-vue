<template>
  <div id="app">
    <v-app id="inspire">
      <v-form ref="form" class="login-form">
        <input
          v-model="email"
          class="email-input"
          type="email"
          placeholder="Email"
          maxlength="40"
          required
        />
        <input
          v-model="password"
          class="email-input"
          type="password"
          placeholder="Password"
          maxlength="20"
          required
        />

        <div class="error-message">{{ message }}</div>
        <v-btn
          :disabled="!(email && password)"
          color="#1877F2"
          class="mr-4"
          @click="login"
        >
          Log In
        </v-btn>
        <a class="forgot">Forgot password ?</a>
        <div color="#42B72A" class="signUp"> <SignUpPopup/> </div>
        
        
      </v-form>
    </v-app>
  </div>
</template>

<script>
import SignUpPopup from "./SignUpPopup.vue"
export default {
  name: "Login",
  components: {SignUpPopup},
  data() {
    return {
      email: "",
      password: "",
      message: "",
      value: false,
    };
  },
  methods: {
    login() {
      (this.value = true), (this.message = "email or password is incorrect");
    },
  },
};
</script>

<style scoped>
#app {
  width: 100%;
   border-radius: 5px;
}
.login-form {
  display: flex;
  flex-direction: column;
  width: 100%;
  justify-content: center;
  align-items: center;
  padding: 15px;
  
  
}
.forgot {
  margin-top: 20px;
  width: 90%;
  display: flex;
  justify-content: center;
  border-bottom: 1px solid #dddfe2;
  padding-bottom: 20px;
}
.error-message {
  color: red;
}

.mr-4 {
  width: 90%;
  color: white;
  margin-left: 4%;
  margin-top: 10px;
}
.signUp {
  margin-top: 20px;
  color: white;
}
.email-input {
  height: 45px;
  width: 90%;
  border-radius: 5px;
  border: 1px solid #dddfe2;
  padding: 5px;
  margin-top: 10px;
}
.email-input:focus {
  border-color: #1877f2;
  box-shadow: 0 0 0 2px #e7f3ff;
  caret-color: #1877f2;
  outline: none !important;
}
#inspire{
    border-radius: 5px;
    box-shadow: 0 2px 4px rgb(0 0 0 / 10%), 0 8px 16px rgb(0 0 0 / 10%);
    margin-right: 10%;
}
</style>
