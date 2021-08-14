<template>
    <div class="chatsW" v-show="none">
        <div class="header">
            <img src="../public/svg/menu.svg" alt="" style="cursor: pointer;">
            <search />
        </div>
        <div class="add">
            <img src="../public/svg/+.svg" alt="">
        </div>
        <div class="ch">
            <div class="chats" @click="chat">
                <chat-windows />
            </div>
            <div class="chats">
                <chat-windows />
            </div>
            <div class="chats">
                <chat-windows />
            </div>
            <div class="chats">
                <chat-windows />
            </div>
            <div class="chats">
                <chat-windows />
            </div>
            <div class="chats">
                <chat-windows />
            </div>
            <div class="chats">
                <chat-windows />
            </div>
            <div class="chats">
                <chat-windows />
            </div>
            <div class="chats">
                <chat-windows />
            </div>
        </div>
    </div>
</template>
<script>
    import ChatWindows from '@/components/ChatWindows.vue'
    export default {
        components: { ChatWindows },
    }
</script>
<style scoped>
    .chatsW
    {
        background: #242E35;
        height: 100vh;
    }
    .header 
    {
        display: flex;
    }
    .header img 
    {
        margin-left: 15px;
        margin-top: 1px;
        margin-right: 7px;
    }
    .search
    {
        width: 90%;
    }
    .add
    {
        width: 56px;
        height: 56px;
        border-radius: 30px;
        background: #7BC411;
        position: fixed;
        left: 45vh;
        top: 90vh;
        display: flex;
        justify-content: center;
        align-items: center;
        cursor: pointer;
    }
    .ch
    {
        overflow-y: scroll;
        height: 90vh;
    }
    .chats
    {
        display: flex;
        align-items: center;
        flex-direction: column;
    }
    @media only screen and (min-width: 500px){
        .chatsW
        {
            width: 600px;
        } 
    }
</style>