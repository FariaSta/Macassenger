<template>
  <div class="containerr">
    <div class="header">
      <maca-logo />
    </div>
    <div class="title">
      <h1>Chat for </br> Friends</h1>
    </div>

    <!-- {{this.ifshowFrom}} -->
    <div class="form" v-if="this.ifshowFrom">
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

    <!--<div class="from" v-else>
      <input-general type="email" placeholder="Email" />
      <input-general type="Password" placeholder="Password" />
      <span>Forgot ytut password?</span>
      <div class="button">
        <button-focus @click="this.ifshowFrom = true"><</button-focus>
        <button-not-focus >Register</button-not-focus>
      </div>
    </div>-->
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

  export default {
    components: {MacaLogo, InputGeneral, ButtonFocus, ButtonNotFocus},
    
    name: 'Home',  
    data(){
      return {
        ifshowFrom: true
      }
    },
    methods: {
      showFrom (){
        this.ifshowFrom = false;
      },
    },
  }

</script>
