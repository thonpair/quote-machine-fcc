<template>
  <div id="app">
    <QuoteBox />
  </div>
</template>

<script>
import QuoteBox from './components/QuoteBox.vue'

export default {
  name: 'App',
  components: {
    QuoteBox
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;

}

</style>
