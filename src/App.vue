<template>
  <div id="app">
    <New />
  </div>
</template>

<script>
  import New from './components/new.vue'
  import Data from './components/Data.vue'
export default {
  name: 'App',
  components:{
  New,
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  width:80%;
  margin:auto;
}
</style>
