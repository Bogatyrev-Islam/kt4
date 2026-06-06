<script setup>
  import Header from './components/Header.vue'
  import Main from './components/Main.vue';
  import Footer from './components/Footer.vue';
</script>

<template>
    <img class="background-image" src="/background-image.jpg" alt="">
    <Header />
    <Main />
    <Footer />
</template>

<style scoped>
  .background-image{
    position: absolute;
    z-index: -10;
    width: 100%;
}
</style>
