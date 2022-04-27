<script>
export default {
    data() {
        return {
            isGood: false,
            likes: 0,
            text: 'Bruh',
        }
    }
}
</script>

<template>
    <h1>📝{{ text }}</h1>
    <div v-if="isGood">
        <h1>👍 Good</h1>
    </div>
    <div v-else>
        <h1>👎 Bad</h1>
    </div>
    <button v-on:click="isGood = !isGood">✨Switch</button>
    <button v-on:click="likes++">👍 {{ likes }}</button>
    <input v-model="text">
</template>

<style>
@import './assets/base.css';

</style>
