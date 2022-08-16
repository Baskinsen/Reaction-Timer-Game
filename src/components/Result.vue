<template>
<p>Reaction TIme: {{score}} ms</p>
<p class="rank">{{rank}}</p>
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
        if(this.score < 200) {
            this.rank = 'Ninja Rapid Fingers'
        } else if (this.score < 400) {
            this.rank = 'Rapid Fingers'
        } else {
            this.rank = 'Snail Fingers'
        }
    }
}
</script>

<style>
    .rank {
        font-size: 1.4em;
        color: #0faf87;
        font-weight: bold;
    }
</style>