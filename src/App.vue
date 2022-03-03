<template>
  <div id="app">
     <AddDesignerWear/>
    <GetDesignerWear/>
  </div>
</template>

<script>
import AddDesignerWear from './components/AddDesignerWear.vue'
import GetDesignerWear from './components/GetDesignerWear.vue'

export default {
  name: 'App',
  components: {
    AddDesignerWear,
    GetDesignerWear,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
