<template>
    <div class="container">
        <router-link to="/">Home</router-link>
        <router-link to="/portfolio">Portfolio</router-link>
        <!--
        <router-link to="/contact">Contact</router-link>
        -->
    </div>
    
</template>

<script>
</script>

<style scoped>
@media screen and (max-width:399px) {
    div {
        height: 7vw;
        background-color:#313131;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    a {
        color: white;
        text-decoration: none;
        text-align: center;
        font-size: 3vw;
        font-family: arial;
        margin-top:1vw;
        margin-bottom: 1vw;
        transition: 0.2s;
        margin-left:2vw;
        margin-right:2vw;
    }

    a:hover {
        font-size: 3.3vw;
        transition: 0.2s;
    }
}
@media screen and (min-width:400px) {
    div {
        height:100%;
        background-color:#313131;
        padding-top:1vw;
    }

    a {
        display: block;
        position:relative;
        color: white;
        text-decoration: none;
        text-align: center;
        font-size: 2vw;
        font-family: arial;
        margin-bottom: 1vw;
        transition: 0.2s;
    }

    a:hover {
        font-size: 2.2vw;
        transition: 0.2s;
    }
}
</style>