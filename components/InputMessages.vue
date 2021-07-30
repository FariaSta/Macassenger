<template>
    <div class="write">
        <input type="text" placeholder="Write..." v-model="messageSend" > 
        <img style="heigth: 35px; width: 35px" src="../public/images/send.png" alt="Send" @click="send">
    </div>
</template>
<script>

import { mapState, mapMutations } from 'vuex' 

export default {
    data() {
        return {
            
        }
    },

    computed: {
        ...mapState(['messageSend'])
        
    },
    methods: {
        ...mapMutations(['send']),

    }
}

</script>
<style scoped>
    .write
    {
        width: 85%;
        display: flex;
        justify-content: center;
    }
    .write input
    {
        width: 100%;
        height: 36px;
        border: 2px solid #7BC411;
        border-radius: 10px;
        background: none;
        color:white;
        padding-left: 10px;
    }
    .write img 
    {
        width: 35px;
        cursor: pointer;
    }
</style>