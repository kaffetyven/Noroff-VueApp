<template> 
    <div class="card__container">      
        <a :href="recipe.href" v-for="recipe in recipes">
          <div class="card" >
            <div class="card__top">
              <div>
                <h1>{{ recipe.title }}</h1>
              </div>
              <div>
                <img :src="recipe.thumbnail">
              </div>
            </div>
            <div>
              <p>{{ recipe.ingredients }}</p>
            </div>  
          </div>         
        </a>          
    </div>      
</template>

<script>

export default {
  name: 'RecipeDumb',
  props: ['recipes']
};

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .card__container{
    display: flex;    
    justify-content: center;
    flex-wrap: wrap;
  }
  a{
    margin:10px;
    border-radius: 15px;
    text-decoration: none;
  }
  h1{
    color: #36495E;
    margin:5px;
  }
  p{
    color: black;
  }
  img{   

  }
  .card{    
    border:solid #42B783 2px;
    border-radius: 5px;  
    padding:15px;
    display: flex;
    flex-direction: column;
    overflow: hidden;
    width:350px;
    height: 180px;
  }
  .card:hover{
    background-image: linear-gradient(to bottom right, white, white, white, white, rgba(66,183,131, 0.5));
    transform: scale(1.03);
  }
  .card__top{
    display: flex;    
    align-items: center;
    justify-content: space-between;
  }
</style>
