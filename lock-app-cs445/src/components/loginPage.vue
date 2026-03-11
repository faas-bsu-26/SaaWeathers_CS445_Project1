<script setup>
import { ref } from 'vue'
import { Password } from 'primevue'

const emit = defineEmits(['login'])
const username = ref('')
const password = ref('')

function handleLogin(){
    if (username.value && password.value){
        emit('login')
    }
}
</script>

<template>
    <div class="phone">

        <h1 class="logo"> DKeys </h1>

        <div class="loginSquares" >

            <input 
                v-model="username" 
                placeholder="Username" />
            <input 
                type="password" 
                v-model="password"
                placeholder="Password" />
        </div>
        
        <button :disabled="!username || !password" 
            @click="handleLogin"> 
            Login 
        </button>
        
        <p class="links"> Sign Up </p>
        <p class="links"> Forgot Password </p>
    </div>
</template>

<style scoped>

.phone{
    width:300px;
    height:600px;
    text-align:center;
    padding:20px;
    outline: 1px solid silver;
    outline-width: 3px;
    border-radius: 32px;
    background: white;
}

.logo{
    padding-top:40px;
    color:black;
    font-size:60px;
    margin-bottom:30px;
}

.loginSquares{
    padding-top:50px;
}
input{
    display:block;
    width:100%;
    margin:10px 0;
    padding:10px;
}

button{
    margin-top:10px;
    padding:10px 20px;
    background: purple;
    color:white;
    border:none;
    border-radius:20px;
}
button:disabled{
    opacity:0.5;
    cursor:not-allowed;
}

.links{
    margin-top: 30px;
    padding-bottom: 5%;
    color: purple;
}

template{
    padding-left:100px;
}

</style>