<template>

    <div class="containerr">
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
        left: 305px;
        top: 571px;
        display: flex;
        justify-content: center;
        align-items: center;
        cursor: pointer;
    }

</style>

<script>
import Search from '@/components/Search.vue'
import ChatWindows from '@/components/ChatWindows.vue'
export default {
    components: {Search, ChatWindows}
}
</script>