<script>
import Menu from './components/Menu.vue';
import Devider from './components/Devider.vue';
import Skills from './components/Skills.vue';
import Projects from './components/Projects.vue';
import Achievements from './components/Achievements.vue';
import Socials from './components/Socials.vue';
import {initFlowbite} from 'flowbite';

export default{
    mounted(){
        initFlowbite()
    },
    components: {
        Menu, Devider, Skills, Projects, Achievements, Socials
    },
    data(){
        return{
            webSkills:[
                { id: 1, name: "HTML5", percentage: "95", photo: "HTML5.png" },
                { id: 2, name: "CSS3", percentage: "90", photo: "CSS3.png" },
                { name: "Sass", percentage: "75", photo: "Sass.png" },
                { name: "Tailwind", percentage: "70", photo: "Tailwind.png" },
                { name: "Bootstrap", percentage: "70", photo: "Bootstrap.png" },
                { name: "Wordpress", percentage: "85", photo: "Wordpress.png" },
                { id: 3, name: "JavaScript", percentage: "65", photo: "JavaScript.png" },
                { name: "React", percentage: "50", photo: "React.webp" },
                { name: "Vue", percentage: "50", photo: "Vue.png" },
                { id: 5, name: "PHP", percentage: "60", photo: "PHP.png" },
                { id: 4, name: "C#", percentage: "55", photo: "CSharp.png" },
                { name: "Java", percentage: "40", photo: "Java.webp" },
            ],
            projects:[
                { name: "Тheatrical Тroupe 'Metafora'", link: "https://studiometafora.com", photo: "studiometafora.png" },
                { name: "Math Manual", link: "https://math.studiometafora.com", photo: "math.png" },
                { name: "Fisica nel Cielo", link: "https://physics.studiometafora.com", photo: "physics.png" },
                { name: "Sunset Diary", link: "https://diary.studiometafora.com", photo: "diary.png" },
                { name: "Talent Factory", link: "https://talentfactory.studiometafora.com", photo: "talentfactory.png" },
                { name: "Брат, не можеш...", link: "https://bratnemozhesh.rayahristova.dev", photo: "bratnemozhesh.png" }
            ],
            wordpressProjects:[
                { name: "Auditing", link: "https://auditingbg.com/", photo: "Auditing.png" },
                { name: "Consult Intellect'", link: "https://consult-intellect.com/", photo: "ConsultIntellect.png" },
                { name: "KrisArt Wedding", link: "https://krisartwedding.com/", photo: "KrisArt.png" },
                { name: "Cteca", link: "https://cteca-sarl.com/", photo: "Cteca.png" },
                { name: "Zalina", link: "https://zalina-ruse.com/", photo: "zalina.png" },
            ],
            achievements:[
                { name: "Methodics and Informtaion Technology in Education (MITE)", project: "Math Manual", stage: "National", place: "Second", location: "Sofia, Bulgaria", date: "14-02-20" },
                { name: "Mathematics & Projecting (Online)", project: "Math Manual", stage: "International", place: "First", location: "Moscow, Russia", date: "18-05-20" },
                { name: "Methodics and Informtaion Technology in Education (MITE)", project: "Fisica nel Cielo", stage: "National", place: "Special price", location: "Stara Zagora, Bulgaria", date: "05-06-21" },
                { name: "Mathematics & Projecting (Online)", project: "Fisica nel Cielo", stage: "International", place: "First", location: "Moscow, Russia", date: "18-05-21" },
                { name: "Methodics and Informtaion Technology in Education (MITE)", project: "Sunset Diary", stage: "National", place: "First", location: "Stara Zagora, Bulgaria", date: "12-03-22" },
                { name: "Mathematics & Projecting (Online)", project: "Sunset Diary", stage: "International", place: "Second", location: "Moscow, Russia", date: "19-05-22" },
                { name: "Certificate of Recognition from Baba Tonka High School of Mathematics", project: "-", stage: "-", place: "-", location: "Ruse, Bulgaria", date: "22-03-22" },
                { name: "Competition for IT, Informatics and Digital Arts (Frontend Development category)", project: "Assignment", stage: "National", place: "13th/53", location: "Devin, Bulgaria", date: "03-06-23" }
            ],
            socials: [
                {name: "Facebook", link: "https://www.facebook.com/raya.thristova22", photo: "fa-facebook-f"},
                {name: "GitHub", link: "https://github.com/thristovaa", photo: "fa-github"},
                {name: "LinkedIn", link: "https://www.linkedin.com/in/raya-hristova-2a135328a", photo: "fa-linkedin-in"},
            ]
        }
    },
    metaInfo: {
        title: 'Raya Hristova | Portfolio',
        meta: [
            {
                name: 'Raya Hristova | Portfolio',
                content: "Hi! I'm Raya Hristova - Frontend Developer. I specialize in creating engaging user-friendly digital experiences that blend aesthetics with functionality. ",
            }
        ],
    },
}

</script>

<template>
    <Menu/>

    <!--Hero-->
    <section class="pt-8 md:pt-32 pb-16" id="home">
        <div class="container flex flex-wrap items-center justify-center mx-auto my-10 md:px-16 md:flex-row">
            <div class="mb-14 lg:mb-0 md:px-8npm run dev lg:w-1/2">
                <h1 class="!text-[3rem] md:!text-[3.5rem] darker-color-text leading-none font-extrabold text-center lg:text-5xl lg:text-left lg:leading-tight mb-5">
                    Hi! I'm Raya Hristova - <span class="font-black text-white text-shadow-glow">Frontend Developer</span>
                </h1>
                <p class="max-w-xl !text-[1.1rem] md:!text-[1.3rem] text-center lg:text-left lg:max-w-md">
                    I specialize in creating engaging user-friendly digital experiences that blend aesthetics with functionality.
                </p>
                <div class="flex justify-center gap-3 mt-14 lg:justify-start">
                    <a type='button' href="/CV.pdf" download class='text-white font-bold rounded-[50px] primary-color-bg px-5 py-4 primary-button transition duration-300 ease-in-out'>Download CV</a>
                </div>
            </div>
            <div class='max-w-[90vw] lg:w-1/2 flex justify-center'>
                <img src="/hero_img.png" alt="hero image" />
            </div>
        </div>
    </section>

    <!--About me-->
    <Devider class="rotate-180" id="about"/>
    <section class="primary-color-bg py-6 md:py-12">
        <div class="container flex flex-wrap items-center justify-center mx-auto gap-5 my-10 md:px-16 md:flex-row">
            <div class='max-w-[90vw] md:max-w-[50vw] flex justify-start'>
                <img src="/about_img.png" alt="hero image" />
            </div>
            <div class="mb-14 lg:mb-0 lg:w-1/2">
                <h2 class="!text-[2.5rem] md:!text-[3rem] text-center font-extrabold text-white text-shadow-glow leading-none lg:text-5xl lg:text-left lg:leading-tight mb-5">
                    About me
                </h2>
                <div class="max-w-[70vw] md:max-w-[50vw] flex flex-col gap-2 text-center lg:text-left">
                    <p class="!text-[1.1rem] font-medium">Hi, my name is Raya Hristova. I'm a developer with a strong foundation in coding and a deep love for frontend development.</p>
                    <p class="!text-[1.1rem] font-medium">With a keen eye for detail and the need to solve different problems, I thrive in the world of software development since the age of 15. I specialize in creating elegant, user-friendly web applications and mobile apps that meet the clients' expectations. My journey in the field of development has equipped me with a skill set, ranging from front-end technologies like HTML, CSS, and JavaScript to back-end languages like PHP.</p>
                    <p class="!text-[1.1rem] font-medium">When I'm not coding, you could find me gazing through books, exploring new songs or enjoying some theatre plays.</p>
                    <p class="!text-[1.1rem] font-medium">I'm confident to say that I am able to turn your vision into reality through the power of code.</p>
                </div>
            </div>
        </div>
    </section>
    <Devider id="skills"/>

    <!--Skills-->
    <section class="py-16">
        <div class="container mx-auto">
            <h2 class="!text-[2.5rem] md:!text-[3rem] mb-12 text-center font-extrabold text-white text-shadow-glow">Skills</h2>
            <div class="flex flex-wrap justify-center items-center mb-12 gap-x-24 md:gap-x-10 gap-10">
                <Skills v-for="item in webSkills" :key="item.key" :percentage="item.percentage" :name="item.name" :photo="item.photo"/>
            </div>
        </div>
    </section>

    <!--Projects-->
    <Devider class="rotate-180" id="projects"/>
    <section class="primary-color-bg py-6 md:py-12 px-6 md:px-0">
        <div class="container mx-auto">
            <h2 class="!text-[2.5rem] md:!text-[3rem] mb-12 text-center font-extrabold text-white text-shadow-glow">Projects</h2>
            <h3 class="!text-[2rem] md:!text-[2.5rem] mb-12 text-center font-extrabold text-white text-shadow-glow">Web Projects</h3>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-12">
                <Projects v-for="item in projects" :link="item.link" :name="item.name" :photo="item.photo"/>
            </div>
            <h3 class="!text-[2rem] md:!text-[2.5rem] mb-12 text-center font-extrabold text-white text-shadow-glow">Wordpress Projects</h3>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <Projects v-for="item in wordpressProjects" :link="item.link" :name="item.name" :photo="item.photo"/>
            </div>
        </div>
    </section>
    <Devider id="achievements"/>

    <!--Achievements-->
    <section class="py-16">
        <div class="container max-w-7xl mx-auto">
            <h2 class="!text-[2.5rem] md:!text-[3rem] mb-12 text-center font-extrabold text-white text-shadow-glow">Achievements</h2>
            <div class='md:min-w-[60vw] py-8'>
                <div class="grid grid-cols-1 gap-10 md:grid-cols-3 md:mx-0 mx-10">
                    <Achievements v-for="item in achievements" :name="item.name" :stage="item.stage" :project="item.project" :place="item.place" :location="item.location" :date="item.date"/>
                </div>
            </div>
        </div>
    </section>

    <!--Footer-->
    <Devider class="hidden md:block rotate-180 animate"/>
    <section class="primary-color-bg py-12 px-6 md:px-0">
        <div class="container flex flex-wrap items-center flex-col justify-center mx-auto my-10 md:px-16 md:flex-row">
            <div class="mb-14 lg:mb-0 lg:w-1/2">
                
                <!--component-->
                <div class="hidden md:flex justify-start flex-col md:flex-row items-center gap-5">
                    <Socials v-for="item in socials" :name="item.name" :link="item.link" :photo="item.photo"/>
                </div>
                <!--component-->
            </div>
            <div class='lg:w-1/2 flex justify-center'>
                Copyright © Raya Hristova, 2023
            </div>
        </div>
    </section>
</template>
