<template> 
    
    <RecipeDumb v-bind:recipes="recipes"/>        
    
</template>

<script>
import RecipeDumb from './RecipeDumb.vue';

export default {
  name: 'RecipeSmart',
  components:{
    RecipeDumb
  },

  data(){
    return{
      recipes: []
    }
  },

  created(){
    const app = this;

    fetch('https://cors-anywhere.herokuapp.com/http://www.recipepuppy.com/api/')
    .then(function(response) {    
      return response.json();
    })
    .then(function(myJson) {      
      app.recipes = myJson.results;    
    });
  }
};


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .container{
    display: flex;
    justify-content: center;        
  } 
  .inline{
    display: inline;
  }
</style>
