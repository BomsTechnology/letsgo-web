<template>
    <div class=" mx-auto max-w-6xl lg:py-20 py-10 flex flex-col items-center justify-center">

        <div>
            <h1 class="text-black font-bold text-2xl lg:text-4xl  leading-normal text-center">Most Frequently visited places </h1>
        </div>

        <div class="grid grid-cols-2 md:grid-cols-3 gap-4 mt-20 lg:px-0 px-4">
            <div class="grid gap-4">
                <CardPlace  v-for="(n, i) in 3" :key="n" :data="data[i]" />
            </div>
            <div class="grid gap-4">
                <CardPlace  v-for="(n, i) in 3" :key="n" :data="data[i + 3]" />
            </div>
            <div class="grid gap-4 grid-cols-2 lg:col-span-1 col-span-2  lg:grid-cols-1">
                <CardPlace  v-for="(n, i) in 3" :key="n" :data="data[i + 6]" />
            </div>
        </div>

        
    </div>
</template>

<script setup lang="ts">
    const data = [
        {
            image: "https://flowbite.s3.amazonaws.com/docs/gallery/masonry/image.jpg",
            name: "National Museum",
            place: "Education, Yde",
        },
        {
            image: "https://flowbite.s3.amazonaws.com/docs/gallery/masonry/image-1.jpg",
            name: "National Museum",
            place: "Education, Yde",
        },
        {
            image: "https://flowbite.s3.amazonaws.com/docs/gallery/masonry/image-2.jpg",
            name: "National Museum",
            place: "Education, Yde",
        },
        {
            image: "https://flowbite.s3.amazonaws.com/docs/gallery/masonry/image-3.jpg",
            name: "National Museum",
            place: "Education, Yde",
        },
        {
            image: "https://flowbite.s3.amazonaws.com/docs/gallery/masonry/image-4.jpg",
            name: "National Museum",
            place: "Education, Yde",
        },
        {
            image: "https://flowbite.s3.amazonaws.com/docs/gallery/masonry/image-5.jpg",
            name: "National Museum",
            place: "Education, Yde",
        },
        {
            image: "https://flowbite.s3.amazonaws.com/docs/gallery/masonry/image-6.jpg",
            name: "National Museum",
            place: "Education, Yde",
        },
        {
            image: "https://flowbite.s3.amazonaws.com/docs/gallery/masonry/image-7.jpg",
            name: "National Museum",
            place: "Education, Yde",
        },
        {
            image: "https://flowbite.s3.amazonaws.com/docs/gallery/masonry/image-8.jpg",
            name: "National Museum",
            place: "Education, Yde",
        }
    ]
</script>