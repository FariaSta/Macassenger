<template>
  <div class="containerr">
    <div class="header">
      <maca-logo />
    </div>
    <div class="title">
      <h1>Chat for </br> Friends</h1>
    </div>

    <!-- Formulary log in -->
    <div class="form" v-if="this.formLogin">
      <input-general type="email" placeholder="Email" />
      <input-general type="Password" placeholder="Password" />
      <span>Forgot your password?</span>
      <div class="button">
        <button-focus >Log in</button-focus>
        <div @click="showFrom">
          <button-not-focus>Register</button-not-focus>
        </div>
      </div>
    </div>

    <!-- Formulary register -->
    <div class="form" v-if="this.formRegister">
      <div class="form__names">
        <input-general class="form__names--name" type="text" placeholder="Name" />
        <input-general type="text" placeholder="Last name" />
      </div>
      <input-general type="email" placeholder="Email" />
      <input-general type="text" placeholder="Username" />
      <input-general type="Password" placeholder="Password" />
      <div class="button2">
          <img style="cursor: pointer " @click="backRegister" src="../public/svg/back.svg" alt="">
        <div >
          <button-focus-large>Register</button-focus-large>
        </div>
      </div>
    </div>

    <footer>
      <span class="inc">© 2021 Macassenger, Inc.</span>
    </footer>
  </div>
  
</template>
<style scoped>
  @import url(../public/style.css);
  .header
  {
    display: flex;
  }
  .containerr
  {
    background: #313F49;
    height: 100%;
  }
  .title
  {
    width: 295px;
    height: 153px;
    margin: 100px 0 67px 9%;
    display: flex;
    align-items: center;
  }
  .title h1 
  {
    color: white;
    font-size: 55px;
    line-height: 75px;
  }
  .form 
  {
    display: flex;
    flex-direction: column;
    text-align: center;
    align-items: center;
    justify-content: center ;
  }
  .form__names input
  {
    width: 150px !important;
  }
  .form__names--name
  {
    margin-right: 10px;
  }
  .inputGeneral
  {
    margin-bottom: 11px;
  }
  span
  {
    color: white;
    font-size: 13px;
    margin-bottom: 14px;
    width: 100%;
    display: flex;
    justify-content: center;
    font-style: normal;
    font-weight: 400;
    line-height: 18px;

  }
  .inc
  {
    margin-top: 10%;
    margin-bottom: 0 !important;
  }
  .button
  {
    display: flex;
    justify-content: space-evenly;
    width: 100%;
  }
  .button2
  {
    display: flex;
    width: 80%;
    justify-content: center;
  } 
  .button2 img
  {
    width: 4%;
    margin-right: 19px;
  } 
  footer
  {
    height: 10vh;
  }

</style>

<script>
  import MacaLogo from '../components/MacaLogo.vue'
  import InputGeneral from '../components/InputGeneral.vue'
  import ButtonFocus from '../components/ButtonFocus.vue'
  import ButtonNotFocus from '../components/ButtonNotFocus.vue'
  import ButtonFocusLarge from '../components/ButtonFocusLarge.vue'

  export default {
    components: {MacaLogo, InputGeneral, ButtonFocus, ButtonNotFocus, ButtonFocusLarge},
    
    name: 'Home',  
    data(){
      return {
        formLogin: true,
        formRegister: false
      }
    },
    methods: {
      showFrom (){
        this.formLogin = false;
        this.formRegister = true;
      },
      backRegister (){
        this.formLogin = true;
        this.formRegister = false;
      }
    },
  }

</script>
