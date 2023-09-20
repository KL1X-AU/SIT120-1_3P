<template>
    <div class="container">
        <a href="https://www.facebook.com/Lachlan.Robinson/" target="_blank">
            <img src="../assets/fb_plain.png">
        </a>
        <a href="https://www.instagram.com/lachlanrobinson_/" target="_blank">
            <img src="../assets/insta_plain.png">
        </a>
        <a href="https://github.com/KL1X-AU" target="_blank">
            <img src="../assets/github_plain.png">
        </a>
    </div>
    
</template>

<script>
</script>

<style scoped>
    div {
        padding: 1vw;
        background-color: #313131;
        height: 100%;
    }
    a {
        display: block;
        height: 4vw;
        width: 3vw;
        position:relative;
    }

    img {
        width: 3vw;
        margin: auto;
        top:0;
        bottom:0;
        left:0;
        right:0;
        margin: auto;
        position: absolute;
        transition: 0.2s-;
    }
    img:hover {
        width: 3.5vw;
        transition:0.2s;
    }

</style>