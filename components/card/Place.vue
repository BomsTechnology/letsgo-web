<template>
    <div class="relative overflow-hidden rounded-3xl">
        <img class="h-full w-full object-cover max-w-full" :src="data.image" alt="">
        <div class="absolute bg-black/50 w-full h-full top-0 left-0 text-white flex items-start justify-end flex-col lg:p-8 px-4 py-6">
            <h2 class=" font-bold text-sm lg:text-2xl leading-5">{{  data.name  }}</h2>
            <p class=" font-light text-xs lg:text-lg lg:mt-2 mt-0.5">{{ data.place }}</p>
        </div>  
    </div>
</template>

<script setup lang="ts">
  export  interface CardPlaceProps {
        image: string;
        name: string;
        place: string;
    }
    const props = defineProps<{
        data: CardPlaceProps;
        }>();
</script>