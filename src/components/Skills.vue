<script>

import { CircleProgressBar } from 'circle-progress.vue';

export default{
    components: {
        CircleProgressBar
    },
    props:{
        photo: String,
        percentage: String,
        name: String
    },
    computed: {
        receivedPhoto() {
            return this.photo;
        },
        receivedPercentage() {
            return this.percentage;
        },
        receivedName() {
            return this.name;
        }
    }
}

</script>

<template>
    <div class="flex flex-col items-center justify-center gap-10 bg-gray-50 pt-6 pb-10 px-5 rounded-full tr-wave bg-contain bg-no-repeat bg-bottom grayscale hover:filter-none transition duration-500 ease-in-out skills">
        <CircleProgressBar :value="receivedPercentage" :colorUnfilled="'#BCA4E3'" :colorFilled="'#BCA4E3'" :max="100" :cx="146" :cy="146" class="bg-gray-200 rounded-full">
            <img :src="'/logos/' + receivedPhoto " class="p-4" style="width: 90px;" alt="HTML">
        </CircleProgressBar>
        <h4 class="!text-[1.2rem] darker-color-text font-bold">{{ receivedName }}</h4>
    </div>
</template>