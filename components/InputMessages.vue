<template>
    <div class="write">
        <input type="text" placeholder="Write...">   
        <img src="../public/images/send.png" alt="Send">
    </div>
</template>
<style scoped>
    .write
    {
        width: 100%;
        display: flex;
        justify-content: center;
    }
    .write input
    {
        width: 85%;
        height: 36px;
        border: 2px solid #7BC411;
        border-radius: 10px;
        background: none;
        color:white;
        padding-left: 10px;
    }
    .write img 
    {
        width: 35px;
        cursor: pointer;
    }
</style>