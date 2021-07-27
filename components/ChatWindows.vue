<template>
    <div class="ChatWindows">
        <div class="chat__face"></div>
        <div class="chat__info">
            <h1>Name Surname</h1>
            <p>Hello. How are you?</p>           
        </div>

    </div>
</template>
<style scoped>
    .ChatWindows
    {
        height: 68px;
        width: 342px;
        border-radius: 10px;
        background: #313F49;
        padding-left: 14px;
        display: flex;
        align-items: center;
        margin-top: 16px;
        cursor: pointer;
    }
    .chat__face
    {
        height: 39px;
        width: 39px;
        border-radius: 30px;
        background: #7BC411;
    }
    .chat__info 
    {
        color: white;
    }
    .chat__info h1
    {
        font-size: 20px;
        margin-bottom: 1px;
        margin-left: 13px;
    }
    .chat__info p 
    {
        font-size: 14px;
        margin-bottom: 0px;
        margin-left: 20px;
    }
</style>