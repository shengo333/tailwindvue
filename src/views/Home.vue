<template>
            <div class="flex justify-center md:justify-end">
                <router-link to="/login">  
                    <a href="#" class="btn text-primary md:border-primary border-2 hover:bg-primary hover:text-white transition ease-out duration-500">Log in</a>
                </router-link> 
                <router-link to="/signup"> 
                    <a href="#" class="btn text-primary ml-2 md:border-primary border-2 hover:bg-primary hover:text-white transition ease-out duration-500">Sign up</a>
                </router-link> 
            </div>
            <header>
                <h2 class="text-gray-700 text-6xl font-semibold">Recipes</h2>
                <h3 class="text-2xl font-semibold">For Ninjas</h3>
            </header>
            <div>
                <h4 class="font-bold mt-12 pb-2 border-b border-gray-200"> Latest Recipes</h4>
                <div class="mt-8 grid lg:grid-cols-3 gap-10"> 
                    <!-- cards go here-->
                    <RecipeCard v-for="recipe in recipes" :recipe="recipe" :key="recipe.title"/>



                </div>
                <h4 class="font-bold mt-12 pb-2 border-b border-gray-200 font">Most populars</h4>
                <div class="mt-8">
                    <!--cards go here-->
                </div>
                <div class="flex justify-center">
                    <div class="btn bg-secondary-100 text-secondary-200 hover:shadow-inner transform hover:scale-125 hower:bg-opacity-50 transition ease-out duration-300">
                       Load more 
                    </div>
                </div>
            </div>
</template>

<script>
import RecipeCard from '../components/RecipeCard.vue'
export default {
  name: 'Recipe',
  components: {
    RecipeCard   
  },
  data(){
      return{
          recipes: [],
     }
  },
  methods: {
      getData() {
          console.log('Getting Data')
          fetch('http://localhost:3000/recipes')
            .then(response => response.json())
            .then(data => this.recipes = data)
            .catch(e => console.log(e))
      }
  },
  mounted() {
      this.getData()
  }
}

</script>