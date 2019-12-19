<template>
  <div id="app" class="container">
    <CountryNavigator/>
  </div>
</template>

<script>
import CountryNavigator from './components/CountryNavigator'
export default {
  name: 'app',
  components: {
    CountryNavigator
  }
}
</script>

<style>
 body{
   background-color: red;
 }
</style>
