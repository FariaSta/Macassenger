<template>
  <div class="containerr">
    <div class="header">
      <maca-logo />
    </div>
    <div class="body">
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
          <picture class="containerback">
            <source class="back" @click="backRegister" srcset="../public/svg/backblack.svg" media="(min-width: 821px)">
            <img class="back" @click="backRegister" src="../public/svg/back.svg" >
          </picture>

          <div >
            <button-focus-large>Register</button-focus-large>
          </div>
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
  .containerback
  {
    width: 45px;
    height: 45px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .back
  {
    cursor: pointer;
    width: 30px !important;
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
  .ButtonFocus
  {
    margin-right: 28px;
  }
  .button
  {
    display: flex;
    justify-content: center;
    width: 100%;
  }
  .button2
  {
    display: flex;
    width: 80%;
    justify-content: center;
    align-items: center;
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

  @media only screen and (min-width: 821px){
    .containerr
    {
      padding-top: 52px;
    }
    .header
    {
      position: absolute;
      top: 100px;
      left: 7%;
      
    }
    .logo
    {
      width: 230px;
      height: 100px;
    }
    .body
    {
      margin-top: 115px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .form
    {
      margin-right: 7%;
      background: white;
      padding: 40px 40px;
      box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.3);
      border-radius: 10px;
    }

    span
    {
      color: #2D2D2D;
    }
    .ButtonNotFocus
    {
      color: #2D2D2D;
    }
    .inputGeneral
    {
      border: 2px solid #2D2D2D;
      color: black;
    }
    .inc
    {
      color: white;
    }
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
