<template>
    <div class="edituser">
        <div class="header">
            <img src="@/public/svg/back.svg" alt="back">
            <h1>Edit User</h1>
        </div>
        <div class="containerUser">
            <div class="img"></div>
            <div class="text">
                <h1>Name Surname</h1>
                <img src="@/public/svg/edit.svg" alt="edit">
            </div>
            <div class="text">
                <h3>@Username</h3>
                <img src="@/public/svg/edit.svg" alt="edit">
            </div>
            
        </div>
    </div>
</template>
<style scoped>
    @import url(../public/style.css);
    .edituser
    {
        background: #242E35;
        color: white;
        height: 100vh;
        width: 100%;
    }
    h1 
    {
        font-size: 30px;
    }
    h3
    {
        font-size: 20px;
        color: #7BC411;
    }
    .containerUser
    {
        display: flex;
        flex-direction: column;
        align-items: center;
        margin-top: 22vh;
    }
    .header
    {
        display: flex;
        height: 8vh;
        align-items: center;
        padding-top: 5px;
    }
    .header img 
    {
        margin-left: 4%;
        
    }
    .header h1 
    {
        margin-left: 29%;
    }
    .img
    {
        margin-bottom: 10px;
        height: 167px;
        width: 167px;
        border-radius: 100px;
        background: #7BC411;
    }
    .text
    {
        display: flex;
        align-items: center;
    }
    .text img
    {
        margin-left: 8px;
    }
</style>