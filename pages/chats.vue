<template>

    <div class="containerr">
        <div class="header">
            <img src="../public/svg/menu.svg" alt="">
            <search />
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

</style>

<script>
import Search from '@/components/Search.vue'
import ChatWindows from '@/components/ChatWindows.vue'
export default {
    components: {Search, ChatWindows}
}
</script>