<script>
export default {
    data() {
        return {
            isGood: false,
            lang: 1,
            likes: 0,
            text: 'Bruh',
            textJP: '不可思議のカルテ',
            textTW: '我有冰淇淋！',
        }
    }
}
</script>

<template>

    <div v-if="lang === 0">
        <h1>📝 {{ textJP }}</h1>
        <div v-if="isGood">
            <h1>👍 良い</h1>
        </div>
        <div v-else>
            <h1>👎 悪い</h1>
        </div>
        <button v-on:click="isGood = !isGood">✨変える</button>
        <button v-on:click="likes++">👍 {{ likes }}</button>
        <button v-on:click="lang++">🌐 言語</button>
        <input v-model="textJP" placeholder="何かを入力"/>
    </div>

    <div v-else-if="lang === 1">
        <h1>📝 {{ text }}</h1>
        <div v-if="isGood">
            <h1>👍 Good</h1>
        </div>
        <div v-else>
            <h1>👎 Bad</h1>
        </div>
        <button v-on:click="isGood = !isGood">✨Switch</button>
        <button v-on:click="likes++">👍 {{ likes }}</button>
        <button v-on:click="lang++">🌐 Language</button>
        <input v-model="text" placeholder="Type Something"/>
    </div>

    <div v-else-if="lang === 2">
        <h1>📝 {{ textTW }}</h1>
        <div v-if="isGood">
            <h1>👍 好屌</h1>
        </div>
        <div v-else>
            <h1>👎 辣雞</h1>
        </div>
        <button v-on:click="isGood = !isGood">✨切換</button>
        <button v-on:click="likes++">👍 {{ likes }}</button>
        <button v-on:click="lang = 0">🌐 語言</button>
        <input v-model="textTW" placeholder="請輸入文字"/>
    </div>

</template>

<style>
@import './assets/base.css';
</style>
