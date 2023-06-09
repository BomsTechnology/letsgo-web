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
            image: "https://i.pinimg.com/originals/dd/8d/85/dd8d851950e92e2e3945d710cbd3a12d.jpg",
            name: "National Museum",
            place: "Education, Yde",
        },
        {
            image: "https://voyage.maresaonline.com/wp-content/uploads/2020/10/5ebbc0c335300_palais-des-sultans-bamouns-ouest-cameroun-maresa-voyage-2-900x600.jpg",
            name: "Foumbam Royal Place",
            place: "Ouest, Bafoussam",
        },
        {
            image: "https://dynamic-media-cdn.tripadvisor.com/media/photo-o/26/74/91/b3/exterior.jpg?w=700&h=-1&s=1",
            name: "Hilton Hotel",
            place: "Education, Yde",
        },
        {
            image: "https://voyage.maresaonline.com/wp-content/uploads/2020/05/5ebaa42d3011f_muse-maritime-douala-bonanjo-cameroun-maresa-voyage.jpg",
            name: "Maritim Museum",
            place: "Bonanjo, Dla",
        },
        {
            image: "https://www.stopblablacam.com/media/k2/items/cache/dacc54c7207467952eb33e27e8047219_L.jpg",
            name: "Playce",
            place: "Warda, Yde",
        },
        {
            image: "https://upload.wikimedia.org/wikipedia/commons/2/26/Les_Gorges_de_Kola2.jpg",
            name: "Les gorges de Kola",
            place: "Nord Cameroun",
        },
        {
            image: "https://afriquexxi.info/IMG/logo/shutterstock_2106094850_3000px.jpg?1654630422",
            name: "Stade olembe",
            place: "Olembe, Yde",
        },
        {
            image: "https://upload.wikimedia.org/wikipedia/commons/3/30/BAFUT_PALACE_-_FON%27S_BUILDING.JPG",
            name: "Fon's Palace",
            place: "Bamenda, Cameroun",
        },
        {
            image: "https://journals.openedition.org/aaa/docannexe/image/2540/img-18-small580.jpg",
            name: "Bameka",
            place: "Ouest Cameroun",
        }
    ]
</script>