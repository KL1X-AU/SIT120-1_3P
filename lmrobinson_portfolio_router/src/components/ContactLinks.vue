<template>
    <div class="container">
        <a href="https://www.facebook.com/Lachlan.Robinson/" target="_blank" id="icon_1">
            <img src="../assets/fb_plain.png">
        </a>
        <a href="https://www.instagram.com/lachlanrobinson_/" target="_blank" id="icon_2">
            <img src="../assets/insta_plain.png">
        </a>
        <a href="https://github.com/KL1X-AU" target="_blank" id="icon_3">
            <img src="../assets/github_plain.png">
        </a>
    </div>
    
</template>

<script>
</script>

<style scoped>
@media  screen and (max-width: 699px) {
    .container {
        background-color: rgb(255, 191, 95);
        width: 30vw;
        height: 10vw;
        border-radius: 5vw;
        display:grid;
        margin-top:2vw;
        margin-bottom: 2vw;
    }
    .divider div {
        background-color: rgb(255, 191, 95);
    }
    a {
        height:clamp(10vw,5%,10vw);
        margin-left:1vw;
        margin-right:1vw;
        display:flex;
        justify-content: center;
        align-items: center;
    }

    img {
        width: 5vw;
        transition:0.2s;
    }
    img:hover {
        width: 6vw;
        transition:0.2s;
    }

    #icon_1 {
        grid-column: 1;
    }
    #icon_2 {
        grid-column: 2;
    }
    #icon_3 {
        grid-column: 3;
    }
}

@media  screen and (min-width: 700px) {
    .container {
        background-color: #313131;
        width: 100%;
        height: 100%;
    }
    a {
        display: block;
        margin:auto;
        position:relative;
        height:clamp(5vw,5%,10vw);
    }

    img {
        width: 3vw;
        top:0;
        bottom:0;
        left:0;
        right:0;
        position: absolute;
        transition: 0.2s;
        margin: auto;
    }
    img:hover {
        width: 3.5vw;
        transition:0.2s;
    }
}
</style>