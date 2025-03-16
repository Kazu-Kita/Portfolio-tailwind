<script setup lang="ts">
defineProps<{
    name:string
    desc:string
    img_path:string
    download_url:string
}>()
import { ref} from 'vue';
const isopen=ref<boolean>(false);
const togglePanel = () => {
    isopen.value=!isopen.value;
}

</script>
<template>
    <div class="w-80 sm:w-100 h-70 mx-auto my-3 bg-gradient-to-br from-blue-100 to-green-100 rounded-xl shadow-md transition-all duration-100 cursor-pointer hover:-translate-y-1 hover:shadow-lg" @click="togglePanel" :class="{ '': !isopen, 'h-100': isopen}">
        <img class="rounded-md mt-2 max-w-xs sm:max-w-98 max-h-60 mx-auto" :src="img_path" alt="">
        <p class="text-3xl">{{ name }}</p>
        <div v-show="isopen === true">
            <a class="block relative text-center my-4 mx-2  bg-white rounded-md duration-200 hover:bg-sky-100" :href="download_url">ダウンロード</a>
            <p class="m-4">{{ desc }}</p>
        </div>
    </div>
</template>