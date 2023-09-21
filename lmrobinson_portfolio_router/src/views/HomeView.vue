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
    import MainHeader from '../components/MainHeader.vue'
    import ContactLinks from '../components/ContactLinks.vue'
    import NavBar from '../components/NavBar.vue'
    import HomeContent from '../components/HomeContent.vue'

    export default {
        name: 'App',
        components: {MainHeader,ContactLinks,NavBar,HomeContent},
    }
</script>

<style>
</style>