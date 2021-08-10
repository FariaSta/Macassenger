<template>

    <div class="containerr">
        <div class="chatsW" v-show="this.windowsview">
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
        <div class="chatP" v-show="this.chatview">
            <div class="title">
                <img class="title__info" src="../public/svg/back.svg" @click="back" alt="back" style="cursor: pointer">
                <face class="title__info" />
                <h1 class="title__info">Name Surname</h1>
            </div>
            <div class="messages">
                <div class="conR">
                    <div class="conR__receiver">
                        <receiver-messages />
                    </div>
                </div>
                <div class="conT"> 
                    <div class="conT__transmitter">
                        <transmitter-messages />
                    </div>    
                </div>     
                <div class="conR">
                    <div class="conR__receiver">
                        <receiver-messages />
                    </div>
                </div>
                <div class="conT"> 
                    <div class="conT__transmitter">
                        <transmitter-messages />
                    </div>    
                </div> 
                <div class="conR">
                    <div class="conR__receiver">
                        <receiver-messages />
                    </div>
                </div>
                <div class="conT"> 
                    <div class="conT__transmitter">
                        <transmitter-messages />
                    </div>    
                </div> 
                <div class="conR">
                    <div class="conR__receiver">
                        <receiver-messages />
                    </div>
                </div>
                <div class="conT"> 
                    <div class="conT__transmitter">
                        <transmitter-messages />
                    </div>    
                </div>           
            </div>
            <div class="inputMessages">
                <input-messages />        
            </div>
        </div>
        <div class="selectchat" v-show="selectchat">
            <h1>Select a chat</h1>
        </div>
        <div class="contact" v-show="contactview">
            <div class="header">
                <img src="../public/svg/back.svg" alt="" style="cursor: pointer;">
                <search />
            </div>
            <div class="containerC">
                <contact />
                <contact />
                <contact />
                <contact />
            </div>
        </div>
    </div>


</template>

<script>
    import Search from '@/components/Search.vue'
    import ChatWindows from '@/components/ChatWindows.vue'
    import InputMessages from '@/components/InputMessages.vue'
    import TransmitterMessages from '@/components/TransmitterMessages.vue'
    import ReceiverMessages from '@/components/ReceiverMessages.vue'
    import Contact from '@/components/Contact.vue'

    export default {
        components: { Search, ChatWindows, InputMessages, ReceiverMessages, TransmitterMessages, Contact },
        data() {
            return {
                windowsview: true,
                chatview: false,
                contactview: false,
                selectchat: true,
                
            }
        },
        methods: {
            back() {
                this.windowsview = true
                this.chatview = false
            },
            chat(){
                this.chatview = true
                this.contactview = false
                this.selectchat = false
            },
            add(){
                this.contactview = false
                this.selectchat = false  
                
            }
        }
    }
</script>

<style scoped>
    @import url(../public/style.css);
    .search
    {
        width: 90%;
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

    .chatsW
    {
        background: #242E35;
        height: 100vh;
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
        height: 81vh;
        padding: 15px 15px 0 15px;
        display: flex;
        flex-direction: column;
        justify-content: initial;
        overflow-y: scroll;
    }
    .conR__receiver
    {
        width: 60%;
    }
    .conT__transmitter
    {
        width: 60%;
    }
    .conR 
    {
        display: flex;
        justify-content: initial;
        margin-bottom: 10px;
    }
    .conT
    {
        display: flex;
        justify-content: end;
        margin-bottom: 10px;
    }
    .inputMessages
    {
        height: 9vh;
        background: #242E35;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .contact
    {
        background: #242E35;
        height: 100%;
    }
    .containerC
    {
        display: flex;
        flex-direction: column;
        align-items: center;
        height: 90vh;
    }
    .selectchat
    {
        width: 100%;
        background: #242E35;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .selectchat h1 
    {
        font-size: 64px;
    }

    @media only screen and (min-width: 500px){
        .containerr
        {
            display: flex;
        }
        .chatsW
        {
            width: 600px;
        }
        .chatP
        {
            width: 100%;
        }
        .title img 
        {
            display: none;
        }


    }
    @media only screen and (max-width: 500px){
        .selectchat
        {
            display: none;

        }


    }

</style>

