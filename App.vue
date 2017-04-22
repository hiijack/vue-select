<template>
  <div id="app">
    <CustomSelect></CustomSelect>
  </div>
</template>

<script>
import CustomSelect from './components/CustomSelect'

export default {
  name: 'app',
  components: {
    CustomSelect
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
}
</style>
