<template>
    <section class="text-white mt-20" id="contact">
        <h2 class="text-4xl font-bold text-white text-left mb-4 px-4 xl:pl-16">Let's Connect</h2>
        <div class="grid md:grid-cols-2 gap-4 relative px-4 xl:px-16 mt-8" data-aos="zoom-in-up">
            <div>
                <p class="text-[#adb7be]">Chamber 1:<br>
                    Rasmono Specialized Hospital, Moghbazar (Next to Aarong), Dhaka.<br>
                    Visiting Hours: <br>
                    [Saturday: 8:30 PM – 10:30 PM] ,[Tuesday & Thursday: 7:30 PM – 9:30 PM]<br>
                    For appointments, 📞 01708-458000 or 0249357766<br>
                </p>
                <p class="text-[#adb7be]"> <br>Chamber 2:<br>
                    Labaid Specialized Hospital, Road No. 4, House No. 6, Dhanmondi, Dhaka (Room No. M60).<br>
                    Visiting Hours: Saturday, Monday & Wednesday: 6:00 PM – 9:00 PM<br>
                    For appointments, 📞 10606 or 02-41060908-18<br>
                </p>

                <!-- Email Section -->
                <div class="flex mb-10 items-center">
                    <div class="p-2"
                        style="background: #111a3e; width: 50px;height: 46px; display: flex;justify-content: center; border-radius: 50%;
                    overflow: hidden;border: 1px solid#111a3e;backdrop-filter: blur(9px);-webkit-backdrop-filter: blur(9px);">
                        <img src="https://img.icons8.com/metro/50/ffffff/new-post.png" alt="new-post" class="w-6">
                    </div>
                    <div class="ml-5 text-white">
                        <h4>Email</h4>
                        <p>cndra42@gmail.com</p>
                    </div>
                </div>

                <!-- Phone Section -->
                <div class="flex mb-10 items-center">
                    <div class="p-2"
                        style="background: #111a3e; width: 50px;height: 46px; display: flex;justify-content: center; border-radius: 50%;
                    overflow: hidden;border: 1px solid#111a3e;backdrop-filter: blur(9px);-webkit-backdrop-filter: blur(9px);">
                        <img src="https://img.icons8.com/ios-filled/50/ffffff/phone.png" alt="phone" class="w-6">
                    </div>
                    <div class="ml-5 text-white">
                        <h4>Phone</h4>
                        <p>+8801718-429680</p>
                    </div>
                </div>

                <!-- LinkedIn Section -->
                <div class="flex mb-10 items-center">
                    <div class="p-2"
                        style="background: #111a3e; width: 50px;height: 46px; display: flex;justify-content: center; border-radius: 50%;
                    overflow: hidden;border: 1px solid#111a3e;backdrop-filter: blur(9px);-webkit-backdrop-filter: blur(9px);">
                        <img src="https://img.icons8.com/ios-filled/50/ffffff/linkedin.png" alt="linkedin" class="w-6">
                    </div>
                    <div class="ml-5 text-white">
                        <h4>LinkedIn</h4>
                        <a href="https://www.linkedin.com/in/chandra-shekhar-karmakar-b64743116/"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="text-white no-underline hover:underline transition">
                            Chandra Shekhar Karmakar
                        </a>
                    </div>
                </div>

                <!-- Facebook Section -->
                <div class="flex mb-10 items-center">
                    <div class="p-2"
                        style="background: #111a3e; width: 50px;height: 46px; display: flex;justify-content: center; border-radius: 50%;
                    overflow: hidden;border: 1px solid#111a3e;backdrop-filter: blur(9px);-webkit-backdrop-filter: blur(9px);">
                        <img src="https://img.icons8.com/ios-filled/50/ffffff/facebook-new.png" alt="facebook" class="w-6">
                    </div>
                    <div class="ml-5 text-white">
                        <h4>Facebook</h4>
                        <a href="https://www.facebook.com/InterventionalPaindoc?rdid=jbFWHNFi8jy2M6U5&share_url=https%3A%2F%2Fwww.facebook.com%2Fshare%2F19x9djxjGZ%2F#"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="text-white no-underline hover:underline transition">
                            Dr. Chandra Shekhar Karmakar
                        </a>
                    </div>
                </div>
            </div>

            <!-- Contact Form -->
            <div
                style="background: #111a3e; width: 100%;height: 100%; border-radius: 20px;
                overflow: hidden;border: 1px solid #111a3e;backdrop-filter: blur(9px);-webkit-backdrop-filter: blur(9px);">
                <form ref="formRef" @submit.prevent="sendEmail" class="flex flex-col p-2" data-aos="zoom-in-up">
                    <h1 class="text-center font-bold text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary text-3xl mb-6"><br>Share Your Thoughts!<br></h1>
                    <div class="mb-6">
                        <label for="name" class="text-white block mb-2 text-sm font-medium">Name</label>
                        <input type="name" id="name" class="bg-[#111827] placeholder:[#9CA2A9] text-gray-100 text-sm rounded-lg block w-full p-2.5"
                        placeholder="Name" name="name">
                    </div>
                    <div class="mb-6">
                        <label for="email" class="text-white block mb-2 text-sm font-medium">Email</label>
                        <input type="email" id="email" class="bg-[#111827] placeholder:[#9CA2A9] text-gray-100 text-sm rounded-lg block w-full p-2.5"
                        placeholder="email@gmail.com" name="email">
                    </div>
                    <div class="mb-6">
                        <label for="subject" class="text-white block mb-2 text-sm font-medium">Subject</label>
                        <input type="subject" id="subject" class="bg-[#111827] placeholder:[#9CA2A9] text-gray-100 text-sm rounded-lg block w-full p-2.5"
                        placeholder="Subject" name="subject">
                    </div>
                    <div class="mb-6">
                        <label for="message" class="text-white block mb-2 text-sm font-medium">Message</label>
                        <textarea id="Message" class="bg-[#111827] placeholder:[#9CA2A9] text-gray-100 text-sm rounded-lg block w-full p-2.5"
                        placeholder="Let's talk about ... " name="Message"></textarea>
                    </div>
                    <button class="z-1 w-[100%!important] px-6 md:px-7 py-3 rounded-full sm:w-max flex justify-center text-white bg-primary border-2 border-transparent">
                        Send Message
                    </button>
                </form>
            </div>
        </div>
    </section>
</template>

<script setup>
import emailjs from '@emailjs/browser';
import { ref } from 'vue';

// Create a ref for the form
const formRef = ref(null);

const sendEmail = () => {
    emailjs.sendForm(
        'service_tzuhtyk',     // EmailJS service ID
        'template_cyrqemn',    // EmailJS template ID
        formRef.value,         // the form DOM element
        'IyRsWrjBOvJGPgptE'    // EmailJS public key
    )
    .then((result) => {
        console.log('SUCCESS!', result.status, result.text);
        alert('Message sent successfully!');
        formRef.value.reset();
    }, (error) => {
        console.error('FAILED...', error);
        alert('Message failed to send.');
    });
};
</script>