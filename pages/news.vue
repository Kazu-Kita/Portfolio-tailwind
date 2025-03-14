<template>
    <div class="text-6xl text-center">News</div>
    <div class="text-center">いろいろお知らせします。</div>
    <div class="w-auto bg-blue-50 m-4 p-4 rounded-3xl" v-for="item in items">
        <div class="text-3xl">{{ item.title }}</div>
        <div>{{ item.date }}</div>
        <div class="mt-8 text-xl">{{ item.content }}</div>
    </div>
</template>
<script setup lang="ts">
    const items=ref([{title:"最初の投稿",date:"2025-03-14",content:"Nuxt勉強中です。"},
    {title:"期末で事故発生",content:"数学Aをやらかしすぎました"},
    {title:"サンプル",content:"サンプル"},
    {title:"サンプル",content:"サンプル"},
    {title:"サンプル",content:"サンプル"},
    {title:"サンプル",content:"サンプル"},
    {title:"サンプル",content:"サンプル"},
    {title:"サンプル",content:"サンプル"},
    {title:"サンプル",content:"サンプル"},
    {title:"サンプル",content:"サンプル"},
    ])
</script>