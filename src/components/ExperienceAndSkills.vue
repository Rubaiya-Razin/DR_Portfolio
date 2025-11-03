<template>
    <section class="text-white mt-18" id="skills">
        <div class="absolute right-0 top-[110rem] h-full w-full justify-end">
            <span class="flex opacity-20">
                <span class="w-16 h-32 rounded-l-full flex bg-primary blur-2xl"></span>
                <span class="w-16 h-32 rounded-r-full flex bg-[#f88fc2] blur-2xl mt-14"></span>
            </span>
        </div>
        <div class="md:grid md:grid-cols-2 gap-8 items-center py-8 px-4 xl:gap-16 xl:px-16">
            <div class="mt-4 md:mt-0 text-left flex flex-col z-10 h-full w-[80%]">
                <h2 class="text-4xl font-bold text-white text-left mb-4">Professional 
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary">Skills</span>
                </h2>
                <div class="mt-8" v-for="skill in Skills" :key="skill.id">
                    <div class="flex items-end justify-between" data-aos="fade-right">
                        <h4 class="text-2xl font-semibold text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary">
                            {{ skill.name }}
                        </h4>
                        <!-- <h3 class="text-2xl font-bold text-white">{{ skill.width }}</h3> -->
                    </div>
                    <!-- <div class="mt-2 h-1 w-full bg-[#131d30] rounded-full">
                        <div class="h-1 rounded-full bg-primary" :style="`width :${skill.width}`"></div>
                    </div> -->
                    <p class="text-white whitespace-pre-line">
                        {{ skill.description }}
                    </p>
                </div>
            </div>
            <div data-aos="flip-left">
                <h2 class="text-4xl font-bold text-white text-left mb-8 md:text-center md:mt-0 mt-8">Experiences</h2>
                <div class="space-y-4 py-4" data-aos="fade-left">
                    <div v-for="element in Experinces" :key="element.id"
                    class="flex  items-center rounded-xl p-4 bg-[#111a3e] shadow-lg border border-[#1f1641]"
                    >
                    <div class="w-1/4">
                        <img src="https://img.icons8.com/ios-filled/100/ffffff/lawyer.png" alt="lawyer">
                    </div>
                    <div class="w-3/4 pl-4">
                        <h3 class="text-2xl font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary">
                            {{ element.role }}
                        </h3>
                        <p class="text-white">{{ element.company }}</p>
                        <p class="text-white">{{ element.date }}</p>
                    </div>
                </div>
                </div>
            </div>
        </div>
    </section>
</template>
<script setup>
import { ref } from 'vue';
const Skills =ref([
    {
        id:1,
        name: 'Pain Management Skills',
        description: 'From simple pain procedures like intra-articular injections,nerve blocks, neurolysis, diagnostic blocks, prolotherapy, pain assessment, and diagnosis of exact causes to creating treatment plans.',

    },
    {
        id:2,
        name:'Advanced procedures',
        // width:'80%'
        description:'Advanced procedures include the most sophisticated treatments for Trigeminal Neuralgia like Gasserian ganglion radiofrequency ablation,chemical ablation, and balloon decompression.',
    },
    {
        id:3,
        name:'For back pain',
        description: 'Epidural steroid injections, selective nerve root blocks, median branch block/RF, vertebroplasty, kyphoplasty for vertebral compression fracture,percutaneous osteoplasty for cancer pain in bone metastases, and neurolysis/gangliolysis in cancer pain.',
    },
    {
        id:4,
        name:'For PLID, spinal canal stenosis, and discogenic pain',
        description: 'Full endoscopic discectomy, thermal annuloplasty, foraminoplasty, and endoscopic spinal canal decompression are performed efficiently.',
    },
    {
        id:5,
        name:'National and international faculty in reputed courses',
        description:'Also worked as a national and international faculty in reputed courses. Conducts 6-month courses in pain medicine to spread knowledge among enthusiastic doctors.',
    },
]);

const Experinces =ref([
    {
        id:1,
        role:'Assistant Professor',
        company:'Bangabandhu Sheikh Mujib Medical University, Dhaka',
        date:'Mar 2021 - Present'
    },
    {
        id:2,
        role:'Junior Consultant',
        company:'Dhaka Medical College and Hospital', 
        date:'Jan 2020 - May 2023'
    },
    {
        id:3,
        role:'Physician',
        company:'Govt Of Bangladesh',
        date:'Aug 2014 - May 2023'
    },
    {
        id:4,
        role:'Medical Officer',
        company:'Ministry of Health & Family Welfare', 
        date:'Aug 2014 - Dec 2019'
    },
    {
        id:5,
        role:'Pain management Fellow',
        company:'Virinchi Hospitals', 
        date:'Sep 2018 - Feb 2019'
    },
    {
        id:6,
        role:'SMO',
        company:'Delta Hospitals Private Limited', 
        date:'May 2012 - Aug 2014'
    },
    {
        id:7,
        role:'RMO',
        company:'Labaid Hospitals and Diagnostics', 
        date:'Dec 2011 - May 2012'
    },
])
</script>
