<template>
    <div class="text-6xl text-center">過去の作品</div>
    <br><br>
    <div class="flex sticky top-16 sm:top-8 h-12 w-76 mx-auto py-1 bg-white/50 backdrop-blur justify-around rounded-xl shadow-md select-none z-999">
        <div class="absolute h-10 w-20 border-2 border-blue-500 rounded-xl" :style="highlightBar"></div>
        <div class="text-3xl cursor-pointer" @click="tab = 1">2023</div>
        <div class="text-3xl cursor-pointer" @click="tab = 2">2024</div>
        <div class="text-3xl cursor-pointer" @click="tab = 3">2025</div>
    </div>
    <div>
        <div v-show="tab === 1" class="flex flex-wrap">
            <Workinfo name="アスレチック" desc="文化祭に出した最初のゲームです。リンクはないのでダミーで許してください" img_path='/image/im.png' download_url="https://example.com"/>
            <Workinfo name="サンプル" desc="写真は適当です。" img_path="image/img2.png" download_url="https://example.com"/>
            <Workinfo name="サンプル" desc="写真は適当です。" img_path="image/kazu.png"/>
            <Workinfo name="サンプル" desc="写真は適当です。" img_path="image/im.png"/>
            <Workinfo name="サンプル" desc="写真は適当です。" img_path="image/im.png"/>
            <Workinfo name="サンプル" desc="写真は適当です。" img_path="image/im.png"/>
            <Workinfo name="サンプル" desc="写真は適当です。" img_path="image/im.png"/>
        </div>
        <div v-show="tab === 2" class="flex flex-wrap">
            <Workinfo name="Swarm" desc="なんちゃらSurvivorsの簡易版を作ってみました"/>
            <Workinfo name="サンプル" desc="要素多めのとき"/>
            <Workinfo name="サンプル" desc="要素多めのとき"/>
            <Workinfo name="サンプル" desc="要素多めのとき"/>
            <Workinfo name="サンプル" desc="要素多めのとき"/>
            <Workinfo name="サンプル" desc="要素多めのとき"/>
            <Workinfo name="サンプル" desc="要素多めのとき"/>
            <Workinfo name="サンプル" desc="要素多めのとき"/>
            <Workinfo name="サンプル" desc="要素多めのとき"/>
            <Workinfo name="サンプル" desc="要素多めのとき"/>
            <Workinfo name="サンプル" desc="要素多めのとき"/>
            <Workinfo name="サンプル" desc="要素多めのとき"/>
            <Workinfo name="サンプル" desc="要素多めのとき"/>
            <Workinfo name="サンプル" desc="要素多めのとき"/>
        </div>
        <div v-show="tab === 3" class="flex flex-wrap">
            <Workinfo name="このウェブサイト" desc="今年最初のまともな作品です。"/>
            <Workinfo name="サンプル" desc="要素多めのとき"/>
            <Workinfo name="サンプル" desc="要素多めのとき"/>
            <Workinfo name="サンプル" desc="要素多めのとき"/>
            <Workinfo name="サンプル" desc="要素多めのとき"/>
            <Workinfo name="サンプル" desc="要素多めのとき"/>
            <Workinfo name="サンプル" desc="要素多めのとき"/>
            <Workinfo name="サンプル" desc="要素多めのとき"/>
            <Workinfo name="サンプル" desc="要素多めのとき"/>
            <Workinfo name="サンプル" desc="要素多めのとき"/>
            <Workinfo name="サンプル" desc="要素多めのとき"/>
            <Workinfo name="サンプル" desc="要素多めのとき"/>
            <Workinfo name="サンプル" desc="要素多めのとき"/>
            <Workinfo name="サンプル" desc="要素多めのとき"/>
        </div>
    </div>
</template>

<script lang="ts">
import { ref, computed} from 'vue';

export default {
    setup() {
        // tab の初期値を1、型を number に指定
        const tab = ref<number>(1);

        const highlightBar = computed(() => {
            return {
                transform: `translateX(${(tab.value - 2) * 100}px)`,
                transition: 'all 0.5s ease', // 位置計算を修正
            };
        });

        return {
            tab,
            highlightBar
        };
    }
}
</script>
