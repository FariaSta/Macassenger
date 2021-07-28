<template>

    <div class="containerr">
        <div class="chatsW" v-show="false">
            <div class="header">
                <img src="../public/svg/menu.svg" alt="" style="cursor: pointer;">
                <search />
            </div>
            <div class="add">
                <img src="../public/svg/+.svg" alt="">
            </div>
            <div class="chats">
                <chat-windows />
                <chat-windows />
                <chat-windows />
                <chat-windows />
                <chat-windows />
                <chat-windows />
                <chat-windows />
                <chat-windows />
                <chat-windows />
                <chat-windows />
                <chat-windows />
                <chat-windows />
                <chat-windows />
            </div>
        </div>
        <div class="chatP" v-show="true">
            <div class="title">
                <img class="title__info" src="../public/svg/back.svg" alt="">
                <face class="title__info" />
                <h1 class="title__info">Name Surname</h1>
            </div>
            <div class="messages">
                <div class="transmitter">
                    <transmitter-messages />
                </div>
                <div class="receiver">
                    <receiver-messages />
                </div>
            </div>
            <div class="inputMessages">
                <input-messages />         
            </div>
        </div>
    </div>


</template>

<style scoped>

    .containerr
    {
        background: #242E35;
    }
    .header
    {
        padding-top: 19px;
        width: 100%;
        display: flex;
    }
    .header img 
    {
        margin-left: 15px;
        margin-top: 1px;
    }
    .chats
    {
        display: flex;
        align-items: center;
        flex-direction: column;
    }
    .add
    {
        width: 56px;
        height: 56px;
        border-radius: 30px;
        background: #7BC411;
        position: fixed;
        left: 80%;
        top: 571px;
        display: flex;
        justify-content: center;
        align-items: center;
        cursor: pointer;
    }

    .title
    {
        height: 10vh;
        width: 100%;
        background: #313F49;
        display: flex;
        align-items: center;
    }
    .title__info
    {
        margin-left: 15px;
    }
    h1 
    {
        font-size: 20px;
        margin-bottom: 1px;
        margin-left: 13px;
        color: white;
    }
    .messages
    {
        background: #242E35;
        height: 80vh;
    }
    .inputMessages
    {
        height: 10vh;
        background: #242E35;
        display: flex;
        justify-content: center;
        align-items: center;
    }

</style>

<script>
import Search from '@/components/Search.vue'
import ChatWindows from '@/components/ChatWindows.vue'
import InputMessages from '@/components/InputMessages.vue'
import TransmitterMessages from '@/components/TransmitterMessages.vue'
import ReceiverMessages from '@/components/ReceiverMessages.vue'
export default {
    components: {Search, ChatWindows, InputMessages, ReceiverMessages, TransmitterMessages}
}
</script>