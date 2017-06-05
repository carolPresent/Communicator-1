<template>
  <div class="container-fluid">
   <div v-if="isSessionNotActive">
     <login v-if="showSignupWindow" :signupButtonAction="toggleSignupLogin" :sessionBeginCallback="sessionBeginCallback"></login>
     <signup v-else :signinButtonAction="toggleSignupLogin"></signup>
   </div>
    <div v-else>
      <conversations></conversations>
    </div>
  </div>
</template>

<script>
    import LoginController from './Login.vue'
    import SignupController from './Signup.vue'
    import ChatScreen from './Chat.vue'

    export default {
    components: {
        'login':  LoginController,
        'signup': SignupController,
        'conversations': ChatScreen
    },
  data() {
      return {
          showSignupWindow: true,
          isSessionNotActive: true
      }
  },
        methods: {
            /*To allow switching from Login to Signup View and vice versa.*/
            toggleSignupLogin () {
                this.showSignupWindow = !this.showSignupWindow;
            },
            /*Inits session based on the flag passed*/
            sessionBeginCallback (isValid) {
                if (!isValid) {
                    alert("Session could not begin. Please try again.");
                    console.log("SESSION: Could not init a session");
                } else {
                    this.isSessionNotActive = !isValid;
                }
            }
        }
}
</script>

