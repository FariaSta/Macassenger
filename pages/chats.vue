<template>

    <div class="chats">
        <div class="header">
            <img src="../public/svg/menu.svg" alt="">
            <search />
        </div>
    </div>

</template>

<style scoped>

    .chats
    {
        background: #313F49;
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

</style>

<script>
import Search from '~/components/Search.vue'
export default {
    components: {Search}
}
</script>