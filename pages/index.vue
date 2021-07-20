<template>
  <div class="containerr">
    <maca-logo />
    <div class="title">
      <h1>Chat for </br> Friends</h1>
    </div>
    
    <form action="/">
      <input-general type="email" placeholder="Email" />
      <input-general type="Password" placeholder="Password" />
      <span>Forgot your password?</span>
      <div class="button">
        <button-focus>Log in</button-focus>
        <button-not-focus>Register</button-not-focus>
      </div>
    </form>
    <span class="inc">© 2021 Macassenger, Inc.</span>



  </div>
  
</template>
<style scoped>
  html 
  {
    height: 100%;
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
  }
  form 
  {
    display: flex;
    flex-direction: column;
    align-items: center;
    
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

</style>

<script>
import MacaLogo from '../components/MacaLogo.vue'
import InputGeneral from '../components/InputGeneral.vue'
import ButtonFocus from '../components/ButtonFocus.vue'
import ButtonNotFocus from '../components/ButtonNotFocus.vue'
export default {
  components: {MacaLogo, InputGeneral, ButtonFocus, ButtonNotFocus}
}
</script>
