<script>
import Menu from './components/Menu.vue';
import Devider from './components/Devider.vue';
import Skills from './components/Skills.vue';
import Projects from './components/Projects.vue';
import {initFlowbite} from 'flowbite';

export default{
    mounted(){
        initFlowbite()
    },
    components: {
        Menu, Devider, Skills, Projects
    },
    data(){
        return{
            webSkills:[
                { id: 1, name: "HTML5", percentage: "100", photo: "HTML5.png" },
                { id: 2, name: "CSS3", percentage: "90", photo: "CSS3.png" },
                { id: 3, name: "JavaScript", percentage: "75", photo: "JavaScript.png" },
                { id: 4, name: "C#", percentage: "65", photo: "CSharp.png" },
                { id: 5, name: "PHP", percentage: "60", photo: "PHP.png" }
            ],
            additionalSkills:[
                { name: "Sass", percentage: "75", photo: "Sass.png" },
                { name: "Tailwind", percentage: "70", photo: "Tailwind.png" },
                { name: "Bootstrap", percentage: "70", photo: "Bootstrap.png" },
                { name: "React", percentage: "50", photo: "React.webp" },
                { name: "Vue", percentage: "50", photo: "Vue.png" },
            ],
            projects:[
                { name: "Тheatrical Тroupe 'Metafora'", link: "studiometafora.com", photo: "studiometafora.png" },
                { name: "Math Manual", link: "math.studiometafora.com", photo: "math.png" },
                { name: "Fisica nel Cielo", link: "physics.studiometafora.com", photo: "physics.png" },
                { name: "Sunset Diary", link: "diary.studiometafora.com", photo: "diary.png" },
                { name: "Talent Factory", link: "talentfactory.studiometafora.com", photo: "talentfactory.png" }
            ]
        }
    }
}

</script>

<template>
    <Menu/>

    <!--Hero-->
    <section class="pt-32 pb-16" id="home">
        <div class="container flex flex-wrap items-center justify-center mx-auto my-10 md:px-16 md:flex-row">
            <div class="mb-14 lg:mb-0 lg:w-1/2">
                <h1 class="!text-[3.5rem] darker-color-text leading-none font-extrabold text-center lg:text-5xl lg:text-left lg:leading-tight mb-5">
                    Hi! I'm Raya Hristova - <span class="font-black text-white text-shadow-glow">Frontend Developer</span>
                </h1>
                <p class="max-w-xl !text-[1.3rem] text-center lg:text-left lg:max-w-md">
                    I specialize in creating engaging user-friendly digital experiences that blend aesthetics with functionality.
                </p>
                <div class="flex justify-center gap-3 mt-14 lg:justify-start">
                    <button type='button' class='text-white font-bold rounded-[50px] primary-color-bg px-5 py-4 primary-button transition duration-300 ease-in-out'>Download CV</button>
                    <button type='button' class='font-bold rounded-[50px] px-5 py-4 primary-color-text text-center secondary-button transition duration-300 ease-in-out'>Projects</button>
                </div>
            </div>
            <div class='lg:w-1/2 flex justify-center'>
                <img src="/hero_img.png" alt="hero image" />
            </div>
        </div>
    </section>

    <!--About me-->
    <Devider class="rotate-180" id="about"/>
    <section class="primary-color-bg py-12">
        <div class="container flex flex-wrap items-center justify-center mx-auto my-10 md:px-16 md:flex-row">
            <div class='lg:w-1/2 flex justify-center'>
                <img src="/about_img.png" alt="hero image" />
            </div>
            <div class="mb-14 lg:mb-0 lg:w-1/2">
                <h2 class="!text-[3rem] text-white text-shadow-glow leading-none font-extrabold text-center lg:text-5xl lg:text-left lg:leading-tight mb-5">
                    About me
                </h2>
                <p class="max-w-xl !text-[1.3rem] text-center lg:text-left lg:max-w-md">
                    I specialize in creating engaging user-friendly digital experiences that blend aesthetics with functionality.
                </p>
                <div class="flex justify-center gap-3 mt-14 lg:justify-start">
                    <button type='button' class='text-white font-bold rounded-[50px] primary-color-bg px-5 py-4 primary-button transition duration-300 ease-in-out'>Socials</button>
                </div>
            </div>
        </div>
    </section>
    <Devider id="skills"/>

    <!--Skills-->
    <section class="py-16">
        <div class="container mx-auto">
            <h2 class="!text-[3rem] mb-3 text-center font-extrabold text-white text-shadow-glow">Skills</h2>
            <h3 class="!text-[2.5rem] mb-12 text-center font-extrabold text-white text-shadow-glow">Web Skills</h3>
            <div class="flex flex-wrap justify-center items-center mb-12 gap-x-10">
                <Skills v-for="item in webSkills" :key="item.key" :percentage="item.percentage" :name="item.name" :photo="item.photo"/>
            </div>
            <h3 class="!text-[2.5rem] mb-12 text-center font-extrabold text-white text-shadow-glow">Additional Skills</h3>
            <div class="flex flex-wrap justify-center items-center mb-12 gap-x-10">
                <Skills v-for="item in additionalSkills" :key="item.key" :percentage="item.percentage" :name="item.name" :photo="item.photo"/>
            </div>
        </div>
    </section>

    <!--Projects-->
    <Devider class="rotate-180" id="projects"/>
    <section class="primary-color-bg py-12 px-6 md:px-0">
        <div class="container mx-auto">
            <h2 class="!text-[3rem] mb-10 text-center font-extrabold text-white text-shadow-glow">Projects</h2>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <Projects v-for="item in projects" :link="item.link" :name="item.name" :photo="item.photo"/>
            </div>
        </div>
    </section>
    <Devider id="achievements"/>

    <!--Achievements-->
    <section class="py-16">
        <div class="container mx-auto">
            <h2 class="!text-[3rem] mb-12 text-center font-extrabold text-white text-shadow-glow">Achievements</h2>
            
        </div>
    </section>

    <!--Footer-->
    <Devider class="rotate-180 animate"/>
    <section class="primary-color-bg py-12 px-6 md:px-0">
        <div class="container flex flex-wrap items-center justify-center mx-auto my-10 md:px-16 md:flex-row">
            <div class="mb-14 lg:mb-0 lg:w-1/2">
                
                    <!--component-->
                    <div class="flex justify-start items-center gap-5">
                        <div class="inline-block h-[60px] w-[60px] overflow-hidden bg-white rounded-[50px] cursor-pointer transition-all duration-300 ease-in-out hover:w-[200px] button">
                           <div class="inline-block h-[60px] w-[60px] text-center rounded-[50px] box-border leading-[60px] transition-all duration-300 ease-in-out icon">
                              <i class="text-[25px] leading-[60px] transition-all duration-300 ease-in-out darker-color-text fab fa-facebook-f"></i>
                           </div>
                           <span class="text-[20px] font-semibold leading-[60px] ml-[10px] transition-all duration-300 ease-out">Facebook</span>
                        </div>
                        <div class="inline-block h-[60px] w-[60px] overflow-hidden bg-white rounded-[50px] cursor-pointer transition-all duration-300 ease-in-out hover:w-[200px] button">
                           <div class="inline-block h-[60px] w-[60px] text-center rounded-[50px] box-border leading-[60px] transition-all duration-300 ease-in-out icon">
                              <i class="text-[25px] leading-[60px] transition-all duration-300 ease-in-out darker-color-text fab fa-github"></i>
                           </div>
                           <span class="text-[20px] font-semibold leading-[60px] ml-[10px] transition-all duration-300 ease-out">Github</span>
                        </div>
                        <div class="inline-block h-[60px] w-[60px] overflow-hidden bg-white rounded-[50px] cursor-pointer transition-all duration-300 ease-in-out hover:w-[200px] button">
                           <div class="inline-block h-[60px] w-[60px] text-center rounded-[50px] box-border leading-[60px] transition-all duration-300 ease-in-out icon">
                              <i class="text-[25px] leading-[60px] transition-all duration-300 ease-in-out darker-color-text fab fa-linkedin-in"></i>
                           </div>
                           <span class="text-[20px] font-semibold leading-[60px] ml-[10px] transition-all duration-300 ease-out">Linkedin</span>
                        </div>
                    <!--component-->
                </div>
            </div>
            <div class='lg:w-1/2 flex justify-center'>
                Random
            </div>
        </div>
    </section>
</template>
