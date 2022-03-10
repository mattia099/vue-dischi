<template>
  <mainHeader />
  <main-content />
</template>

<script>
import mainHeader from './components/mainHeader.vue'
import mainContent from './components/mainContent.vue'

export default {
  name: 'App',
  components: {
    mainHeader,
    mainContent
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

img{
  max-width: 100%;
}
</style>
