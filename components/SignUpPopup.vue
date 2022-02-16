<template>
  <div class="a">
    <v-row justify="center">
      <v-dialog v-model="dialog" persistent max-width="450px">
        <template v-slot:activator="{ on, attrs }">
          <v-btn color="success" class="btn" dark v-bind="attrs" v-on="on">
            Create New Account
          </v-btn>
        </template>
        <v-card>
          <v-card-title class="header">
            <div>
              <span class="text-h5">Sign Up</span>
              <p>Its quick and easy</p>
            </div>

            <img
              @click="dialog = false"
              class="_8idr img"
              src="https://static.xx.fbcdn.net/rsrc.php/v3/yC/r/Q0G2UVjVQ4_.png"
              alt=""
              width="24"
              height="24"
              id="u_5_9_Fb"
            />
          </v-card-title>
          <div class="signUp-popup">
            <v-form ref="form" class="SignUp-form">
              <input
                v-model="firstName"
                class="name-input"
                type="text"
                placeholder="First name"
                maxlength="20"
                required
              />
              <input
                v-model="lastName"
                class="name-input"
                type="text"
                placeholder="Last name"
                maxlength="20"
                required
              />
            </v-form>
            <v-form ref="form" class="email-password">
              <input
                v-model="email"
                class="e-input"
                type="text"
                placeholder="Mobile number or Email "
                maxlength="40"
                required
              />
              <input
                v-model="password"
                class="e-input"
                type="password"
                placeholder="New password"
                maxlength="20"
                required
              />
            </v-form>
            <Datepicker />
            <div class="radio-group">
              <v-card flat>
                <v-card-text>
                  <div class="gender">
                    <p>Gender</p>
                    <img
                      class="icon"
                      src="https://img.icons8.com/emoji/48/000000/white-question-mark-emoji.png"
                    />
                  </div>
                  <v-container fluid>
                    <v-row>
                      <v-row class="all-radio" cols="3" sm="1" md="1">
                        <v-radio-group v-model="ex8" row>
                          <v-radio
                            label="Female"
                            color="primary"
                            value="female"
                            class="radio-btn"
                          
                          ></v-radio>
                          <v-radio
                            label="Male"
                            color="primary"
                            value="male"
                            class="radio-btn"
                          ></v-radio
                          ><v-radio
                            label="Custom"
                            color="primary"
                            value="custom"
                            class="radio-btn"
                          ></v-radio>
                        </v-radio-group>
                      </v-row>
                    </v-row>
                    <p class="paragraph">By clicking Sign Up, you agree to our Terms, Data Policy and Cookie Policy. You may receive SMS notifications from us and can opt out at any time.</p>
                  </v-container>
                </v-card-text>
              </v-card>
            </div>
          </div>
          <v-card-actions class="signupBtn">
            <v-btn class="mr-4" color="success" @click="dialog = false" :disabled="disabled()">
              Sign Up
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>
    </v-row>
  </div>
</template>

<script>
import Datepicker from "./DatePicker.vue";
export default {
  name: "SignUpPopup",
  components: { Datepicker },
  data() {
    return {
      dialog: false,
      ex8: "",
      email: "",
      password: "",
      firstName: "",
      lastName: "",
      
    };
  },
  methods: {
disabled(){
  if(this.email&&this.password&&this.firstName&&this.lastName&&this.ex8){
    return false;
  }else{
    return true;
  }
  
}
  },
 
};
</script>

<style>
.text-h5 {
  font-weight: bold;
}
.header {
  display: flex;
  justify-content: space-between;
  border-bottom: 1px solid #dddfe2;
  height: 90px;
}
.text-h5 {
  font-weight: bolder !important;
}
.v-application .text-h5 {
  font-size: 2.2rem !important;
}
.header p {
  font-size: 0.9rem;
  font-weight: 400 !important;
  color: #606770;
  margin-top: -5px !important;
}
.header div {
  width: 50%;
}
.SignUp-form {
  display: flex;
  width: 100%;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
}
.name-input {
  height: 45px;
  width: 48%;
  border-radius: 5px;
  border: 1px solid #dddfe2;
  padding: 5px;
  margin-top: 10px;
  background-color: #f5f6f7;
}
.name-input:focus {
  border-color: #1877f2;
  box-shadow: 0 0 0 2px #e7f3ff;
  caret-color: #1877f2;
  outline: none !important;
}
.signUp-popup {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.email-password {
  display: flex;
  flex-direction: column;
  justify-content: center;
  width: 91.5%;
  margin-top: -18px;
}
.e-input {
  height: 45px;
  width: 100%;
  border-radius: 5px;
  border: 1px solid #dddfe2;
  padding: 5px;
  margin-top: 10px;
  background-color: #f5f6f7;
}
.e-input:focus {
  border-color: #1877f2;
  box-shadow: 0 0 0 2px #e7f3ff;
  caret-color: #1877f2;
  outline: none !important;
}

.radio-btn {
  padding: 10px;
  width: 126px;
  padding: 10px 20px 10px 10px;
  border-radius: 5px;
  border: 2px solid #dddfe2;
  height: 35px;
}

.all-radio {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-left: 2px;
  margin-top: -30px;
}
.icon {
  background-color: #606770;
  height: 15px;
  width: 15px;
  border-radius: 50%;
  margin-left: -40px;
  margin-top: 23px;
}
.gender {
  display: flex;
  margin-left: 3px;
  font-weight: 300;
  font-size: 0.8rem;
  margin-top: -20px;
}
.mr-4 {
  width: 50%;
  color: white;
  margin-left: 60px;
  margin-top: -30px;
  margin-bottom: 25px
}
.btn {
  margin-top: 10px;
  margin-bottom: 17px;
}
.signupBtn {
  width: 90%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.img {
  margin-top: -40px;
  margin-right: -15px;
}
.img:hover{
  cursor: pointer;
}
.paragraph{
   font-weight:400 !important;
   font-size:11px;
   width:100%;
}
.v-overlay__scrim{
  background-color: #fff !important;
}
</style>
