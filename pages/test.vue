<template>
    <div class="containerr">
        <chats-w /> 
        <chat-p />
        <select-chat />
    </div>
</template>
<script>
import ChatsW from '@/components/ChatsW.vue'
import ChatP from '@/components/ChatP.vue'
import SelectChat from '@/components/SelectChat.vue'
export default {
    components: { ChatsW, ChatP, SelectChat }
}
</script>
<style scoped>
    @media only screen and (min-width: 500px){
        .containerr
        {
            display: flex;
        }
    }
</style>