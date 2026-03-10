<script setup>
import { ref } from 'vue'
//import different pages for different locks
//add settings dropdown, work on back buttons and logout
//move image for dropdown to right of page
const emit = defineEmits(['openLock'])

const locks = ref([
    'Front Door',
    'Garage',
    'Office',
    'Back Door'
])
</script>

<template>

    <div class="phone">

        <div class="header">
            DK
            <img src="/Users/kenxn/Downloads/monster-2.png" alt="Logo" />
        </div>

        <h3>Welcome, Username</h3>

        <h4>Your Locks</h4>

        <div v-for="lock in locks" class="lock" @click="emit('openLock')">
            {{lock}}
        </div>


    </div>

</template>


<style scoped>

.phone{
    width:300px;
    margin:auto;
}

.header{
    background:purple;
    color:white;
    padding:15px;
}

.header img {
    padding: 10px;
    width: 50px;               /* adjust image size */
    height: 50px;
    object-fit: contain;       /* keep aspect ratio */
}

.lock{
    border-bottom:1px solid black;
    padding:10px;
    
}

</style>