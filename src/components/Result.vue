<template>
    <p>Reaction Time : {{score}} ms</p>
    <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
    props:['score'],
    data (){
        return{
            rank: null
        }
    },
    mounted(){
        if(this.score <250){
            this.rank = "You're too fast bro"
        }else if(this.score <400){
            this.rank = "You're good bro"
        }else{
            this.rank = "You're slow bro"
        }
    }
}
</script>

<style>
    .rank{
        font-size: 1.4em;
        color: #0faf87;
        font-weight: bold ;
    }
</style>