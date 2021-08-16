<template>
    <div class="chatP">
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
</template>
<script>
    import ReceiverMessages from '@/components/ReceiverMessages.vue'
    import TransmitterMessages from '@/components/TransmitterMessages.vue'
    import InputMessages from '@/components/InputMessages.vue'
    import Face from '@/components/Face.vue'
    export default {
        components: { ReceiverMessages, TransmitterMessages, InputMessages, Face },
    }
</script>
<style scoped>
    .chatP
    {
        width: 100%;
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
</style>