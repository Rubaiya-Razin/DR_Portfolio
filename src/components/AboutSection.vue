<template>
    <section class="text-white mt-18" id="about">
        <div class="absolute z-0 top-[93rem] inset-x-0 h-64 flex items-start">
            <div class="h-24 w-64 bg-gradient-to-br from-primary via-secondary blur-2xl to-[#570cac] opacity-20"></div>
        </div>
        <div class="md:grid md:grid-cols-2 gap-8 items-center py-8 px-4 xl:gap-16 sm:py-16 xl:px-16 z-1">
            <div data-aos="flip-right">
                <h2 class="text-4xl font-bold text-white text-left mb-8">Education</h2>
                <div class="space-y-8 py-8">
                    <div v-for="element in education" :key="element.id"
                    class="flex items-center md:w-[80%] w-full rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641]"
                    >
                        <div class="w-1/4">
                            <img src="https://img.icons8.com/ios-glyphs/60/ffffff/graduation-cap--v1.png" alt="graduation-cap--v1">
                        </div>
                        <div class="w-3/4 pl-4">
                            <h3 class="text-2xl font-semibold text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary lg:text-xl">
                                {{ element.School }}
                            </h3>
                            <p class="text-white">{{ element.program }}</p>
                            <p class="text-white">{{ element.year }}</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="mt-4 md:mt-0 text-left flex flex-col z-10 h-full" data-aos="flip-right">
                <h2 class="text-4xl font-bold text-white md:text-center text-left mb-4">More
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary">About</span>
                    Dr. Chandra
                </h2>
                <p class="text-base lg:text-lg mt-1 py-1">
                    Dr. Chandra Shekhar graduated with an MBBS degree from Mymensingh Medical College in 2010. He then achieved the FCPS (Anesthesiology) from BCPS with distinction, successfully completing both Part I and Part II on his very first attempt. In 2018, he was awarded a fully funded fellowship by the World Federation of Societies of Anesthesiologists, which he completed with excellence at Virinchi Hospital in Hyderabad, South India, specializing in Interventional Pain Management. During this fellowship, he was mentored by internationally acclaimed pain medicine expert Dr. Murlidhar Joshi. Under Dr. Joshi’s guidance, Dr. Shekhar received hands-on training in all forms of advanced pain management procedures.
                </p>
                <p v-if="showMore" class="text-base lg:text-lg mt-1 py-1">
                    Upon returning to Bangladesh, he joined Shaheed Suhrawardy Medical College Hospital as a Registrar, where he initiated the Pain Clinic and performed the country's first-ever chemical ablation of the Gasserian ganglion for trigeminal neuralgia. This landmark procedure marked a significant advancement in pain treatment in Bangladesh. He also introduced and successfully carried out a wide range of modern pain interventions such as Gasserian ganglion ablation, radiofrequency ablation, vertebroplasty, percutaneous osteoplasty, and endoscopic discectomy.
                    <br><br>
                    In 2022, Dr. Shekhar completed advanced training in Musculoskeletal Ultrasound and Pain Medicine from the Kalinga Institute of Medical Sciences. In 2024, he obtained the European Diploma of Pain Medicine (EDPM), an internationally recognized qualification in pain management, successfully passing both the first and second parts on his initial attempt. He then went on to complete a fellowship in spinal endoscopy under the mentorship of Dr. Girish Datar, a renowned endoscopic spine surgeon based in Miraj, Maharashtra. Dr. Shekhar became the first Bangladeshi pain physician to successfully perform endoscopic discectomy in the country.
                    <br><br>
                    To date, he has successfully performed hundreds of advanced pain management procedures, including vertebroplasty, Gasserian ganglion ablation, celiac plexus neurolysis, stellate ganglion blocks, percutaneous spinal endoscopy, and DiscFX treatments. His research has been published in various national and international journals, and he regularly serves as a faculty member in both domestic and international training programs. At present, Dr. Chandra Shekhar is serving as an Assistant Professor in the Department of Anesthesiology, Analgesia, and Intensive Care Medicine at Bangabandhu Sheikh Mujib Medical University (BSMMU).
                </p>
                <button @click="showMore = !showMore" class="text-primary underline mt-2">
                    {{ showMore ? 'Read Less' : 'Read More' }}
                </button>
                <div class="grid grid-cols-3 gap-4 max-w-lg pt-8">
                    <div class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-3">
                        <h3 class="text-white font-bold text-xl sm:text-2xl lg:text-3xl">+2000</h3>
                        <p class="text-sm sm:text-base text-gray-300">Happy Patient</p>
                    </div>
                    <div class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-3">
                        <h3 class="text-white font-bold text-xl sm:text-2xl lg:text-3xl">+2500</h3>
                        <p class="text-sm sm:text-base text-gray-300">Patients</p>
                    </div>

                    <div class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-3">
                        <h3 class="text-white font-bold text-xl sm:text-2xl lg:text-3xl">+13</h3>
                        <p class="text-sm sm:text-base text-gray-300"> Years Experience</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
<script setup>
import { ref } from 'vue';

const showMore = ref(false); // Add this line to define the showMore variable

const education = ref([
    {
        id: 1,
        School: 'Mymensingh Medical College',
        program: 'MBBS, Medicine, Surgery, Obs and Gynaecology',
        year: '2005 - 2011',
    },
    {
        id: 2,
        School: 'Bangladesh College Of Physicians And Surgeons.',
        program: 'FCPS, Anaesthesiology',
        year: '2012 - 2017',
    },
    {
        id: 3,
        School: 'Virinchi Hospital,  Hyderabad',
        program: 'WFSA Pain Medicine Fellowship',
        year: 'July 2018- January 2019',
    },
    {
        id: 4,
        School: 'The European Society of Regional Anaesthesia and Pain Therapy',
        program: 'European Diploma in Pain Medicine(EDPM)',
        year: '2024',
    },
]);
</script>