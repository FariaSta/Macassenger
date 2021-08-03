<template>
  <div class="search">
    <input  placeholder="Search">
    <img class="back" src="../public/svg/search.svg" >
  </div>

  
</template>

<style scoped>

  .search
  {
    height: 10vh;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  input
  {
    width: 85%;
    height: 36px;
    border: 2px solid #7BC411;
    border-radius: 10px;
    background: none;
    color:white;
    font-size: 20px;
    text-align: left;
    padding: 0 0 0 15px;
  }
  img
  {
    cursor: pointer;
    margin-left: 15px;
  }



</style>