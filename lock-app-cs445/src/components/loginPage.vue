<script setup>
const emit = defineEmits(['login'])
</script>

<template>
    <div class="phone">
        <h1 class="logo"> DKeys </h1>

        <input placeholder="Username" />
        <input type="password" placeholder="Password" />

        <button @click="emit('login')"> Login </button>
        
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
    outline: 1px solid blue;
}

.logo{
    font-size:60px;
    margin-bottom:30px;
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

.links{
    color: purple;
}

</style>