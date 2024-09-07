<script setup>
import { onMounted, ref, watch } from "vue";
import ChildComp from "./components/ChildComp.vue";

let count = ref(0);
let title = "Hello Vue";
let color = ref("red");

onMounted(() => {
    console.log("mounted!");
});
watch(color, () => {
    console.log("color!!");
});

const increaseCount = () => {
    count.value++;
};
</script>

<template>
    <div>
        <h1>{{ title }}</h1>
        <button @click="increaseCount">count++</button>
        <p>{{ count }}</p>
        <ChildComp :color="color" bgColor="yellow" />
        <button @click="color = 'green'">change color</button>
    </div>
</template>

<style scoped></style>
