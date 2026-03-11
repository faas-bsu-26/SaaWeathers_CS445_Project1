<script setup>
import { ref } from 'vue'
//import different pages for different locks
//add settings dropdown, work on back buttons and logout
//move image for dropdown to right of page
const emit = defineEmits(['openLock'])

const locks = ref([
    'Front Door'
])
</script>

<template>

    <div class="phone">

        <div class="header">
            DK
            <button class="settingsDropdown">
                <img src="/Users/kenxn/Downloads/dropdown_button_white.jpg" alt="Dropdown" />

            </button>
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
    margin: auto;
    height:600px;
    text-align:center;
    outline: 1px solid silver;
    outline-width: 3px;
    border-radius: 32px;
    background: white;
}

.header{
    background:purple;
    color:white;
    padding:15px;
    border-top-left-radius: 32px;
    border-top-right-radius: 32px;
}

.header img {
    padding: 10px;
    width: 50px;               
    height: 50px;
    object-fit: contain;       
}

.lock{
    border-bottom:1px solid black;
    padding:10px;
    
}

</style>