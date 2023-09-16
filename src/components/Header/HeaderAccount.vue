<script setup>
    defineProps({
        loggedIn: {
            type: Boolean,
            required: true
        }
    })
</script>

<template>
    <div v-if="loggedIn">
        <div class="profile">
            <img src="" alt="">
        </div>
    </div>

    <div class="login" v-else>
        <a href="">
            <h2>Login</h2>
        </a>
    </div>
</template>

<style scoped>
    .login{
        width: 130px;
        height: 42px;
        flex-shrink: 0;
        border-radius: 2px;
        border: 2px solid #FFF;

    
    }


    .login:hover{
        border: 2px solid #1a8dc2;
    }
    .login:hover a{
        background-color: #b81366;
    }

    .login:hover a h2{
        color: #fcb000;
    }

    a{
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    h2{
        color: #FFF;
        text-align: center;
        font-size: 16px;
        font-style: normal;
        font-weight: 500;
        line-height: normal;
    }
    
</style>