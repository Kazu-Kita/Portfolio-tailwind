<template>
    <Header></Header>
    <div class="absolute mt-48 left-64 w-[calc(100%-256px)]">
        <div class="text-4xl text-center">過去の作品</div>
        <br><br>
        <div class="flex w-76 mx-auto bg-blue-100 justify-around">
            <div class="text-xl" @click="tab = 1">2023</div>
            <div class="text-xl" @click="tab = 2">2024</div>
            <div class="text-xl" @click="tab = 3">2025</div>
        </div>
        <div class="">
            <div v-show="tab === 1" class="">
                <Workinfo name="アスレチック" desc="文化祭に出した最初のゲームです。"/>
                <Workinfo name="アスレチック" desc="文化祭に出した最初のゲームです。"/>
                <Workinfo name="アスレチック" desc="文化祭に出した最初のゲームです。"/>
                <Workinfo name="アスレチック" desc="文化祭に出した最初のゲームです。"/>
            </div>
            <div v-show="tab === 2" class="">
                <Workinfo name="Swarm" desc="なんちゃらSurvivorsの簡易版を作ってみました"/>
            </div>
            <div v-show="tab === 3" class="">
                <Workinfo name="このウェブサイト" desc="今年最初のまともな作品です。"/>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
export default{
    data: ()=>{
        return{
            tab:1,
        }
    }
}
</script>

<style>
    .tabbar{
        display:flex;
    }
</style>