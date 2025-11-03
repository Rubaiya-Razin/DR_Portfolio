<template >
    <section class="text-white mt-20" id="testimonials" data-aos="zoom-in">
        <h2 class="text-4xl font-bold text-white text-left mb-4 px-4 xl:pl-16">Satisfied Patient Reviews</h2>
        <div class="px-4 xl:px-16">
            <Carousel v-bind="settings" :breakpoints="breakpoints" >
                <Slide v-for="element in testimonials" :key="element.id">
                    <div class="carousel__item p-4">
                        <div class="w-full mx-auto bg-[#111a3e] shadow-lg border border-[#1f1641] p-5 text-white font-light mb-6">
                            <div class="w-full flex mb-4 items-center">
                                <div class="overflow-hidden rounded-full w-10 h-10 bg-gray-50 border border-gray-200">
                                    <img :src="element.image" alt="testimonial image" loading="lazy">
                                </div>
                                <h6 class="ml-4 font-bold text-sm uppercase text-white">{{ element.fullName }}</h6>
                            </div>
                            <div class="w-full">
                                <p class="text-sm leading-tight">
                                    <span class="text-lg leading-none italic font-bold text-white mr-1">"</span>
                                        {{ element.comment }}
                                    <span class="text-lg leading-none italic font-bold text-white mr-1">"</span>
                                </p>
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
import { Carousel , Navigation , Slide } from 'vue3-carousel';
import 'vue3-carousel/dist/carousel.css';
//Carousel settings
const settings =ref({
    itemsToShow:1,
    snapAlign:"center",
})

//Breakpoints
const breakpoints =ref({
    700:{
        itemsToShow:2.5,
        snapAlign:'center',
    },
    1024:{
        itemsToShow:3,
        snapAlign:'start'
    }
})

const testimonials=ref([
    {
        id:1,
        fullName:'Patient 1',
        image:'src/assets/patient.png',
        comment:'Dr. Chandra Shekhar Karmakar is truly an expert in pain management. His treatment significantly reduced my chronic back pain, and I can finally enjoy daily activities again. Highly recommended! – Razin'
    },
    {
        id:2,
        fullName:'Patient 2',
        image:'src/assets/patient.png',
        comment:'I had been suffering from severe knee pain for years, but after Dr. Karmakar’s treatment, I feel so much better. He listens carefully, explains everything clearly, and provides the best care.– Mariam S'
    },
    {
        id:3,
        fullName:'Patient 3',
        image:'src/assets/patient.png',
        comment:'I was nervous about my treatment, but Dr. Karmakar made me feel at ease. His approach is patient-centered, and the results speak for themselves. I am pain-free after years of suffering! – Nusrat J.'
    },
    {
        id:4,
        fullName:'Patient 4',
        image:'src/assets/patient.png',
        comment:'Excellent doctor with a kind heart! My mother’s chronic arthritis pain has improved drastically under his care. We are forever thankful!  - Razin'
    },
    {
        id:5,
        fullName:'Patient 5',
        image:'src/assets/patient.png',
        comment:'A compassionate and highly skilled doctor! The spine procedure he performed worked wonders for me. I am grateful for his dedication and expertise. – Tanvir A.'
    },
])
</script>
<style >
    .carousel__prev,.carousel__next {
        color: white !important;
    }
</style>