<script setup lang="ts">
defineProps<{
    name:string
    desc:string
    path:string
}>()
</script>
<template>
    <div class="w-64 h-76 bg-blue-100 shadow-l">
        <img :src="path" alt=""></img>
        <p class="text-xl">{{ name }}</p>
        <p class="text-l">{{ desc }}</p>
    </div>
</template>