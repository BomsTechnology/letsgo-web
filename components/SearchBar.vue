<template>
    <div class="w-full flex justify-center flex-col items-center gap-6">
        <div class="bg-white rounded-lg lg:rounded-full max-w-5xl w-full flex items-stretch overflow-hidden">
            <div class="flex flex-wrap w-full lg:w-5/6">
                <input type="text" placeholder="Enter destination" class=" lg:w-1/5 w-1/2 border-0 border-r  rounded-l-full text-sm lg:text-base lg:pl-4 lg:py-6 pt-6 pl-6 pb-4 foucs:outline-none focus:ring-0">
                <input type="text" placeholder="Departure Location" class=" lg:w-1/5 w-1/2 border-0 lg:border-r  foucs:outline-none text-sm lg:text-base pl-4 lg:py-6 pt-6 pb-4 focus:ring-0">
                <input type="text" placeholder="Departure Date & Time" class=" lg:w-1/5 w-1/2  border-t border-r  lg:border-t-0 border-0 text-sm lg:text-base lg:text-left text-center lg:pl-6 px-4 lg:py-2 py-4 focus:outline-0 focus:ring-0">
                <input type="text" placeholder="Seats" class=" lg:w-1/5 w-1/2 border-t lg:border-r  lg:border-t-0 border-0 text-sm lg:text-base lg:text-left text-center lg:pl-6 px-4 lg:py-2 py-4 focus:outline-0 focus:ring-0">
                <input type="text" placeholder="Budget" class=" lg:w-1/5 w-full border-t lg:border-t-0 border-0 text-sm lg:text-base lg:text-left text-center lg:pl-6 px-4 lg:py-2 py-4 focus:outline-0 focus:ring-0">
            </div>

                <button type="button" class="text-white bg-secondary w-1/6 h-full font-medium justify-center focus:ring-4 focus:outline-none focus:ring-primary rounded-r-full text-xs lg:text-base px-5 py-2.5 text-center lg:inline-flex hidden items-center dark:bg-secondary dark:hover:bg-secondary dark:focus:ring-secondary">
                    <span>Rechercher</span>    
                </button>

            
        </div>
        <button type="button" class="text-white bg-secondary lg:w-1/4 font-medium justify-center   focus:ring-4 focus:outline-none focus:ring-primary rounded-full text-sm sm:text-base px-5 py-2.5 text-center inline-flex lg:hidden items-center dark:bg-secondary dark:hover:bg-secondary dark:focus:ring-secondary">
            <span>Rechercher</span>    
        </button>
    </div>
</template>

<script setup lang="ts">

</script>
