<template>
	<div id="app">	
	<h1>Javascript Frameworks Module Assignment 2:</h1>
    <RecipeSmart/>
  </div>
</template>

<script>
import RecipeSmart from './components/RecipeSmart.vue';

export default {
  name: 'app',
  components: {
    RecipeSmart
  }
};
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
