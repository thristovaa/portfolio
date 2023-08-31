<script>
    export default{
        props:{
            photo: String,
            link: String,
            name: String
        },
        computed: {
            receivedPhoto() {
                return this.photo;
            },
            receivedLink() {
                return this.link;
            },
            receivedName() {
                return this.name;
            }
        }
    }
</script>

<template>
    <div class="flex flex-col bg-white rounded-[50px]">
        <img :src="'/projects/' + receivedPhoto" class="rounded-tl-[50px] rounded-tr-[50px] min-w-[20vw]" alt="">
        <div class="p-6 flex justify-between items-center">
            <h4 class="!text-[1.2rem] darker-color-text font-bold">{{ receivedName }}</h4>
            <div class="primary-color-bg p-3 flex items-center justify-center rounded-full skills transition duration-300 ease-in-out">
                <a class="p-0 m-0 !max-h-[20px]" :href="receivedLink">
                    <ion-icon name="chevron-forward-outline" style="color: #fff; min-height:2vh; font-size:20px"></ion-icon>
                </a>
            </div>
        </div>
    </div>
</template>