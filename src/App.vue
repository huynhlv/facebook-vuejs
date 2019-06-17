<template>
  <div>
    <Header />
    <Home />
  </div>
</template>  

<script>
  import Header from './components/Shared/Header.vue'
  import Home from './components/HomePage/Home.vue'
  export default {
    components: {
      Header,
      Home
    }
  }
</script>

<style lang="scss" src="./assets/style.scss"></style>
