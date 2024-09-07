<template>
    <div>
        <h2>Child Componet</h2>
        <p :style="{ color: color, backgroundColor: bgColor }">{{ color }}</p>
    </div>
</template>
<script setup>
const props = defineProps({
    color: String,
    bgColor: String,
});
</script>
<style></style>
