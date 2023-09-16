<script setup>
    import IconDocumentation from './icons/IconDocumentation.vue';
</script>

<template>
    <div id="logo">
        <a href="#">
            <IconDocumentation />
            <h2>
                GamificaAção
            </h2>
        </a>
    </div>
</template>

<style scoped>
    #logo{
        display: flex;
        flex-direction: row;
        width: 200px;
        height: auto;
        gap: 10px;
        align-items: center;
        vertical-align: middle;
    }

    a{
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 15px;
    }

    h2{
        color: #fff;
    }
</style>