<!--
vue의 구성요소는: 컴포넌트->사용자의 인터페이스와 특정부분을 캡슐화하는 것
재사용 가능하고 독립적인 코드 조각으로 사용하는것
-->

<template>
<div v-on:click="countClicks">
<h1>{{ foodName }}</h1>
<img src="../assets/img/img_quality.svg" v-show="isFavorite">
<p>{{ foodDesc }}</p>
<h2>{{name}}</h2>
<p>{{message}}</p>
<p id="red">
저를 {{clicks}} 번 클릭하셨내요
</p>
</div>
</template>
<script>
export default{
    props:[
        'foodName','foodDesc','isFavorite'
    ],
    data(){
        return{
        name:'황영일',
        message:'맥도날드',
        clicks:0
        }       
    },
    methods:{
        countClicks(){
            this.clicks++
        }
    }

}
</script>
<style>
#red{
    font-weight:bold; color:rgb(144, 12, 12)
}
img{
    height: 1.5em;
    float: right;
}
</style>

<!--뷰의 주성문 기호는 html과 동일-->


