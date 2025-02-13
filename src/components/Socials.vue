<script>
    export default{
        props:{
            link: String,
            name: String,
            photo: String
        },
        computed: {
            receivedLink() {
                return this.link;
            },
            receivedName() {
                return this.name;
            },
            receivedPhoto() {
                return this.photo;
            }
        }
    }
</script>

<template>
    <div class="inline-block h-[60px] w-[60px] overflow-hidden bg-white rounded-[50px] cursor-pointer transition-all duration-300 ease-in-out hover:w-[200px] button">
        <div class="inline-block h-[60px] w-[60px] text-center rounded-[50px] box-border leading-[60px] transition-all duration-300 ease-in-out icon">
            <a :href="receivedLink" target="_blank"><i :class="'text-[25px] leading-[60px] transition-all duration-300 ease-in-out darker-color-text fab ' + receivedPhoto "></i></a>
        </div>
        <span class="text-[20px] font-semibold leading-[60px] ml-[10px] transition-all duration-300 ease-out">{{ receivedName }}</span>
    </div>
</template>