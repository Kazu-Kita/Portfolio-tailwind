<script setup lang="ts">
defineProps<{
    name:string
    desc:string
    path:string
}>()
import { ref} from 'vue';
const isopen=ref<boolean>(false);
const togglePanel = () => {
    isopen.value=!isopen.value;
}

</script>
<template>
    <div class="w-auto min-w-64 h-76 mx-auto my-3 bg-gradient-to-br from-blue-200 to-pink-200 rounded-xl shadow-md transition-all duration-500" @click="togglePanel" :class="{ '': !isopen, 'h-100': isopen}">
        <img class="rounded-md h-67" :src="path" alt="">
        <p class="text-xl">{{ name }}</p>
        <div v-show="isopen === true">
            <p class="text-l">{{ desc }}</p>

        </div>
    </div>
</template>