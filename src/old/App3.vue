
<template>  <!--html이 template-->
<h1>Food</h1>
<p>v-for가 컴포넌트를 배열로 만들어 줍니다</p>
<div class="" id="wrapper">
    <food-item
        v-for="x in foods"
        v-bind:food-name="x"
    />  <!--컴포넌트다-->
</div>
</template>

<script>
export default{ //데이터를 컴포넌트안에 담아주는것
    data(){
        return{
            foods:['사과','피자','쌀','물고기','cake']
        };
    }
}
</script>


<style>
#wrapper{
    display: flex;
    flex-wrap: warp;
}
#wrapper>div{
    border: dashed black 2px;
    margin: 10px;
    padding: 0 20px;
    background-color: hotpink;
}
</style>