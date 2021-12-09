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
                    <RecepCard />
                    <div class="card hover:shadow-lg">
                        <img src="../assets/stew.jpg" alt="stew" class="w-full h-32 sm:h-48 object-cover">
                        <div class="m-4">
                        <router-link to="/Stew">
                                <span class="font-bold"> 5 Bean Chilli Stew</span>
                                <span class="block text-gray-500 text-sm">Recipe from Mario</span>
                            </router-link>
                        </div>
                        <div class="badge">
                            <svg xmlns="http://www.w3.org/2000/svg" class="w-5 inline-block" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
                              </svg>
                            <span>25 Mins</span>
                        </div>
                    </div>
                    <div class="card hover:shadow-lg">
                        <img src="../assets/noodles.jpg" alt="noodles" class="w-full h-32 sm:h-48 object-cover">
                        <div class="m-4">
                            <router-link to="/noodles">
                                <span class="font-bold"> Veg Noodles</span>
                                <span class="block text-gray-500 text-sm">Recipe from Mario</span>
                            </router-link>
                        </div>
                        <div class="badge">
                            <svg xmlns="http://www.w3.org/2000/svg" class="w-5 inline-block" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
                              </svg>
                            <span>25 Mins</span>
                        </div>
                    </div>
                    <div class="card hover:shadow-lg">
                        <img src="../assets/curry.jpg" alt="curry" class="w-full h-32 sm:h-48 object-cover">
                        <div class="m-4">
                            <router-link to="/curry">
                                <span class="font-bold"> Tofu Curry</span>
                                <span class="block text-gray-500 text-sm">Recipe from Mario</span>
                            </router-link>
                        </div>
                        <div class="badge">
                            <svg xmlns="http://www.w3.org/2000/svg" class="w-5 inline-block" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
                              </svg>
                            <span>25 Mins</span>
                        </div>
                    </div>
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

import RecepCard from '../components/RecepCard.vue'


export default {
  name: 'Recept',
  components: {
    RecepCard   
  },
  data(){
      return{
          recipes: [
              {
                  img: '../assets/stew.jpg',
                  time: '25 Mins',
                  title: '5 Bean Chilli Stew',
                  author:  'Recipe from Mario'
              },
              {
                  img: '../assets/noodles.jpg',
                  time: '25 Mins',
                  title: 'Veg Noodles',
                  author:  'Recipe from Mario'
              },
              {
                  img: '../assets/curry.jpg',
                  time: '25 Mins',
                  title: 'Tofu Curry',
                  author:  'Recipe from Mario'
              },
          ]
      }
  }
}
</script>