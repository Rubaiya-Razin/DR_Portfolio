<template>
    <section class="text-white mt-20" id="gallery" data-aos="zoom-in">
        <h2 class="text-4xl font-bold text-white text-left mb-4 px-4 xl:pl-16"><br><br><br>Gallery</h2>
        <div class="px-4 xl:px-16">
            <Carousel v-bind="settings" :breakpoints="breakpoints">
                <Slide v-for="element in gallery" :key="element.id">
                    <div class="carousel__item p-4">
                        <div class="w-full mx-auto bg-[#111a3e] shadow-lg border border-[#1f1641] p-5 text-white font-light mb-6">
                            <div class="w-full">
                                <img :src="element.image" alt="gallery image" class="w-full h-auto rounded-lg" loading="lazy">
                            </div>
                        </div>
                    </div>
                </Slide>
                <template #addons>
                    <Navigation />
                </template>
            </Carousel>
        </div>
    </section>
</template>

<script setup>
import { ref } from 'vue';
import { Carousel, Navigation, Slide } from 'vue3-carousel';
import 'vue3-carousel/dist/carousel.css';

// Carousel settings
const settings = ref({
    itemsToShow: 3, // Default: Show 3 images side by side
    snapAlign: "center",
    wrapAround: true, // Enable infinite scrolling
    transition: 500, // Transition speed in milliseconds
});

// Breakpoints for responsiveness
const breakpoints = ref({
    0: {
        itemsToShow: 1, // Show 1 image on small screens
        snapAlign: 'center',
    },
    768: {
        itemsToShow: 2, // Show 2 images on medium screens
        snapAlign: 'center',
    },
    1024: {
        itemsToShow: 3, // Show 3 images on large screens
        snapAlign: 'start',
    },
});

// Gallery data
const gallery = ref([
    {
        id: 1,
        image: 'src/assets/pro_pic1.jpg',
    },
    {
        id: 2,
        image: 'src/assets/pro_pic2.jpg',
    },
    {
        id: 3,
        image: 'src/assets/pro_pic3.jpg',
    },
    {
        id: 4,
        image: 'src/assets/pro_pic4.jpg',
    },
    {
        id: 5,
        image: 'src/assets/pro_pic5.jpg',
    },
    {
        id: 6,
        image: 'src/assets/pro_pic6.jpg',
    },
    {
        id: 7,
        image: 'src/assets/pro_pic7.jpg',
    },
    {
        id: 8,
        image: 'src/assets/pro_pic8.jpg',
    },
    {
        id: 9,
        image: 'src/assets/pro_pic9.jpg',
    },
]);
</script>

<style>
.carousel__prev,
.carousel__next {
    color: white !important;
}
</style>