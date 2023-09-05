<script>
    export default{
        props:{
            name: String,
            project: String,
            stage: String,
            place: String,
            location: String,
            date: String
        },
        computed: {
            receivedName() {
                return this.name;
            },
            receivedProject() {
                return this.project;
            },
            receivedStage() {
                return this.stage;
            },
            receivedPlace() {
                return this.place;
            },
            receivedLocation() {
                return this.location;
            },
            receivedDate() {
                return this.date;
            }
        }
    }
</script>

<template>
    <div class="flex flex-col justify-between flex-1 min-w-[22vw] bg-white px-12 py-8 gap-4 rounded-[50px] shadow overflow-hidden relative border-effect">
        <div class="background-layer hidden md:block"></div>
        <div class="z-10 flex flex-col gap-3">
            <h3 class="darker-color-text text-xl font-bold">{{ receivedName }}</h3>
            <h4><span class='font-semibold darker-color-text text-lg'>Project: </span>{{ receivedProject }}</h4>
        </div>
        <div class='z-10 flex gap-5 justify-between'>
            <div>
                <span class='font-semibold darker-color-text text-lg'>Stage: </span><p>{{ receivedStage }}</p>
                <span class='font-semibold darker-color-text text-lg'>Place: </span><p>{{ receivedPlace }}</p>
            </div>
            <div>
                <span class='font-semibold darker-color-text text-lg'>Location: </span><p>{{ receivedLocation }}</p>
                <span class='font-semibold darker-color-text text-lg'>Date: </span><p>{{ receivedDate }}</p>
            </div>
        </div>
    </div>
</template>