<template>
    <nav  :class="[ isScroll ? 'fixed z-50 w-full bg-white shadow text-white' : 'fixed w-full bg-transparent text-white dark:bg-gray-800']">
    <div :class="[isScroll ?  'py-4 ' : 'py-8 ']" class="container px-6 mx-auto md:flex md:justify-between md:items-center">
        <div class="flex items-center justify-between">
            <a href="#">
                <img v-if="isScroll" class=" h-12 w-auto lg:h-16" src="~/assets/images/logo.png" alt="">
                <img v-else class=" h-12 w-auto lg:h-16" src="~/assets/images/logo1.png" alt="">
            </a>

            <!-- Mobile menu button -->
            <div class="flex lg:hidden">
                <button  @click="isOpen = !isOpen" type="button" :class="[ isScroll ? 'text-gray-700' : 'text-white']" class="dark:text-gray-200 hover:text-gray-600 dark:hover:text-gray-400 focus:outline-none dark:focus:text-gray-400" aria-label="toggle menu">
                    <svg  v-if="!isOpen" xmlns="http://www.w3.org/2000/svg" class="w-6 h-6 " fill="currentColor" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M4 8h16M4 16h16" />
                    </svg>
            
                    <svg v-if="isOpen" xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
                    </svg>
                </button>
            </div>
        </div>

        <!-- Mobile Menu open: "block", Menu closed: "hidden" -->
        <div  :class="[isOpen ? 'translate-x-0 opacity-100 ' : 'opacity-0 -translate-x-full']" class="absolute inset-x-0 z-20 w-full px-6 py-4 sm:mt-0 mt-4 transition-all duration-300 ease-in-out bg-white dark:bg-gray-800 md:mt-0 md:p-0 md:top-0 md:relative md:bg-transparent md:w-auto md:opacity-100 md:translate-x-0 md:flex md:items-center">
            <div class="flex flex-col md:flex-row md:mx-6">
                <a :class="[ isScroll ? 'text-gray-700' : 'sm:text-white text-gray-700 ']" class="my-2 transition-colors duration-300 transform dark:text-gray-200 hover:text-blue-500 dark:hover:text-blue-400 md:mx-8 md:my-0 text-sm sm:text-base font-medium" href="#">Covoiturage</a>
                <a :class="[ isScroll ? 'text-gray-700' : 'sm:text-white text-gray-700 ']" class="my-2 transition-colors duration-300 transform dark:text-gray-200 hover:text-blue-500 dark:hover:text-blue-400 md:mx-8 md:my-0 text-sm sm:text-base font-medium" href="#">Bus</a>
                <a :class="[ isScroll ? 'text-gray-700' : 'sm:text-white text-gray-700 ']" class="my-2 transition-colors duration-300 transform dark:text-gray-200 hover:text-secondary dark:hover:text-blue-400 md:mx-8 md:my-0 text-sm sm:text-base font-medium" href="#">Taxi</a>
                <a :class="[ isScroll ? 'text-gray-700' : 'sm:text-white text-gray-700 ']" class="my-2 transition-colors duration-300 transform dark:text-gray-200 hover:text-secondary dark:hover:text-blue-400 md:mx-8 md:my-0 text-sm sm:text-base font-medium" href="#">Moto</a>
                <a :class="[ isScroll ? 'text-gray-700' : 'sm:text-white text-gray-700 ']" class="my-2 transition-colors duration-300 transform dark:text-gray-200 hover:text-secondary dark:hover:text-blue-400 md:mx-8 md:my-0 text-sm sm:text-base font-medium" href="#">Tarifs</a>
                <a :class="[ isScroll ? 'text-gray-700' : 'sm:text-white text-gray-700 ']" class="my-2  transition-colors duration-300 transform dark:text-gray-200 hover:text-secondary dark:hover:text-secondary md:mx-8 md:my-0 text-sm sm:text-base font-medium" href="#">Trajets</a>
                <a :class="[ isScroll ? 'text-gray-700' : 'sm:text-white text-gray-700 ']" class="my-2  transition-colors duration-300 transform dark:text-gray-200 hover:text-secondary dark:hover:text-secondary md:mx-8 md:my-0 text-sm sm:text-base font-medium" href="#">Partenaires</a>
            </div>

            <div class="flex justify-center md:block sm:mt-0 mt-4">
                <button type="button" class="text-white bg-secondary font-medium justify-center sm:w-auto w-full focus:ring-4 focus:outline-none focus:ring-primary rounded-full text-sm sm:text-base px-5 py-2.5 text-center inline-flex items-center dark:bg-secondary dark:hover:bg-secondary dark:focus:ring-secondary">
                    <span>Se Connecter</span>    
                </button>
            </div>
        </div>
    </div>
</nav>
</template>

<script setup lang="ts">
    const isOpen = ref(false);
    const isScroll = ref(false);
    onMounted(() => {
        window.addEventListener("scroll", async function () {
                isScroll.value = window.scrollY > 150;
        });     
    })
</script>