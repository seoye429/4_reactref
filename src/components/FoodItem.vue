<template>
<h2>
    {{ foodName }}
    <img src="../assets/img/stamp.svg" v-show="foodIsFavorite"/>
</h2>
<p>{{ foodDesc }}</p>
<button v-on:click.stop="toggleFavorite">추구미</button>
</template>

<script>
export default{
    props:['foodName','foodDesc','isFavorite'],
    data(){
        return{
            foodIsFavorite: this.isFavorite
        }
    },
    methods:{
        toggleFavorite(){
            this.foodIsFavorite = !this.foodIsFavorite; //!는 같지 않다면
        }
    }
}
</script>

<style>
img{
    height: 1.5em;
    float: right;
}
</style>