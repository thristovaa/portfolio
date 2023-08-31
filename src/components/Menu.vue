<template>
  <nav :class="['w-[100vw] fixed z-20 bg-cover bg-center h-[7rem] menu-devider-bg transition-all duration-500 ease-in-out animate', { 'scrolled': isScrolled }]" id="scrolled">
    <ul class="flex items-center justify-center h-full">
      <li class="mx-4">
        <a @click="scrollToSection('home')" class="cursor-pointer darker-color-text font-extrabold menu-item transition-all duration-300 ease-in-out text-[18px] hover:text-white">Home</a>
      </li>
      <li class="mx-4">
        <a @click="scrollToSection('about')" class="cursor-pointer darker-color-text font-extrabold menu-item transition-all duration-300 ease-in-out text-[18px] hover:text-white">About me</a>
      </li>
      <li class="mx-4">
        <a @click="scrollToSection('skills')" class="cursor-pointer darker-color-text font-extrabold menu-item transition-all duration-300 ease-in-out text-[18px] hover:text-white">Skills</a>
      </li>
      <li class="mx-4">
        <a @click="scrollToSection('projects')" class="cursor-pointer darker-color-text font-extrabold menu-item transition-all duration-300 ease-in-out text-[18px] hover:text-white">Projects</a>
      </li>
      <li class="mx-4">
        <a @click="scrollToSection('achievements')" class="cursor-pointer darker-color-text font-extrabold menu-item transition-all duration-300 ease-in-out text-[18px] hover:text-white">Achievements</a>
      </li>
    </ul>
  </nav>
</template>

<script>
  export default {
    name: 'Menu',
    data() {
      return {
        isScrolled: false,
      };
    },
    mounted() {
      window.addEventListener('scroll', this.handleScroll);
    },
    beforeDestroy() {
      window.removeEventListener('scroll', this.handleScroll);
    },
    methods: {
      handleScroll() {
        this.isScrolled = window.scrollY > 0;
      },
      scrollToSection(sectionId) {
        const element = document.getElementById(sectionId);
        if (element) {
          window.scrollTo({
            top: element.offsetTop,
            behavior: 'smooth',
          });
        }
      }
    },
  }
</script>