<template>
    <div class="grid-container">
        <div id="header">
            <MainHeader />
        </div>
        <div id="contactbar">  
            <ContactLinks />
        </div>
        <div id="navbar">  
            <NavBar/>
        </div>
        <div id="content">
            <HomeContent/>
        </div>
    </div>
    
    
</template>

<script>
    import MainHeader from './components/MainHeader.vue'
    import ContactLinks from './components/ContactLinks.vue'
    import NavBar from './components/NavBar.vue'
    import HomeContent from './components/HomeContent.vue'

    export default {
        name: 'App',
        components: {MainHeader,ContactLinks,NavBar,HomeContent},
    }
</script>

<style>
    body {
        margin:0;
        height:100vh;
    }

    .grid-container {
        width: 100%;
        height: 100%;
        display: grid;
        grid-template-columns: 10vw 40vw 45vw 5vw;
        grid-template-rows: auto auto auto;
    }

    #header {
        grid-column-start: 1;
        grid-column-end: 5;
        grid-row-start:1;
        grid-row-end:1;
    }

    #contactbar {
        grid-column-start: 4;
        grid-column-end: 5;
        grid-row-start: 2;
        grid-row-end: 3;
        height: 100%;
    }

    #navbar {
        grid-column-start: 1;
        grid-column-end: 2;
        grid-row-start: 2;
        grid-row-end: 2;
    }

    #content {
        grid-column-start: 2;
        grid-column-end: 4;
        grid-row-start: 2;
        grid-row-end: 2;
    }
</style>