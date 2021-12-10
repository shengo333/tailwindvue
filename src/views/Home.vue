<template>
    <div class="md:grid grid-cols-3"> <!-- content wrapper -->
        <div class="md:col-span-1 md:flex md:justify-end">
            <Navigation />
        </div> <!-- end nav -->
        <main class="px-16  py-6 bg-gray-100 md:col-span-2">
            <Recipe />
        </main>
    </div>
</template>

<script>
// @ is an alias to /src
import '@/assets/tailwind.css'
import Navigation from '../components/Navigation.vue'
import Recipe from '../components/Recipe.vue'
import RecipeCard from '../components/RecipeCard.vue'


export default {
  name: 'Home',
  components: {

    Navigation,
    Recipe,


    
  }
}
</script>
