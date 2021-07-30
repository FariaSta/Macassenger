<template>
    <div class="TransmitterMessages">
        <p>{{ messageSend }}</p>
    </div>
</template>
<script>
    import { mapState, mapMutations } from 'vuex' 

    export default {
        computed: {
            ...mapState(['messageSend'])
        }
    }

</script>
<style scoped>

    .TransmitterMessages
    {
        color: white;
        padding: 0px 10px; 
        border: 2px solid #7BC411;
        border-radius: 10px;
    }
</style>
