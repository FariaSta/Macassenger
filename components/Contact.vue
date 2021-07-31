<template>
    <div class="ChatWindows">
        
        <div class="chat__info">
            <face />
            <div style="display: flex; align-items: center">
                <h1>Name Surname</h1>
            </div>
           
        </div>

    </div>
</template>
<style scoped>
    .ChatWindows
    {
        height: 68px;
        width: 90%;
        padding-left: 14px;
        display: flex;
        align-items: center;
        margin-top: 16px;
        cursor: pointer;
    }
    .chat__info 
    {
        display: flex;
        color: white;
    }
    .chat__info h1
    {
        font-size: 20px;
        margin-bottom: 1px;
        margin-left: 13px;
    }
    .chat__info p 
    {
        font-size: 14px;
        margin-bottom: 0px;
        margin-left: 20px;
    }
</style>
<script>
import Face from '../components/Face.vue'
export default {
    components: { Face }
}
</script>