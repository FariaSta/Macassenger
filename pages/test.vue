<template>
    <div class="containerr">
        <chats-w /> 
        <contact-view />
        <chat-p />
        <select-chat />
        <edit-user />
    </div>
</template>
<script>
import ChatsW from '@/components/ChatsW.vue'
import ChatP from '@/components/ChatP.vue'
import SelectChat from '@/components/SelectChat.vue'
import ContactView from '@/components/ContactView.vue'
import EditUser from '@/components/EditUser.vue'
export default {
    components: { ChatsW, ChatP, SelectChat, ContactView, EditUser }
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