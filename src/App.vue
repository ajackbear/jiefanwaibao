<template>
  <div id="app">
    <u-header></u-header>
    <router-view/>
  </div>
</template>

<script>
import UHeader from './components/header/header.vue'
export default
{
  name: 'App',
  components:
  {
    "u-header": UHeader
  }
}
</script>

<style lang="css">
@import "./styles/reset.css";
</style>
