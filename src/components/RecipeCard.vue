<template>
    <div class="card hover:shadow-lg">
        <img :src="require(`@/assets/${recipe.img}`)" alt="stew" class="w-full h-32 sm:h-48 object-cover">
        <div class="m-4">
        <router-link to="/Stew">
                <span class="font-bold"> {{recipe.title}}</span>
                <span class="block text-gray-500 text-sm">{{recipe.author}}</span>
            </router-link>
        </div>
        <div class="badge">
            <svg xmlns="http://www.w3.org/2000/svg" class="w-5 inline-block" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
            </svg>
            <span>{{recipe.time}}</span>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        recipe: Object
    }    
}
</script>