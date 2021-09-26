<template>
    <p>Reaction time : {{ score }} ms</p>
    <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
    props: ['score'],
    data() {
        return {
            rank: null
        }
    },
    mounted() {
        if(this.score < 250) {
            this.rank = "Ninja Fingers!🤴"
        } else if (this.score < 400) {
            this.rank = "Rapid Reflexes!😎"
        } else {
            this.rank = "Snail pace...🙃"
        }
    },
}
</script>

<style>
    .rank {
        color: rgb(18, 206, 18);
        font-size: 6vh;
        font-weight: 600;
    }
</style>