<template>
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
</template>
<script>
    import Contact from '@/components/Contact.vue'
    export default {
        components: { Contact }
    }
</script>
<style scoped>
    .contact
    {
        background: #242E35;
        height: 100%;
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
    .containerC
    {
        display: flex;
        flex-direction: column;
        align-items: center;
        height: 90vh;
    }
</style>