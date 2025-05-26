<template>
<h1>Food</h1>
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse, perferendis.</p>
<div class="" id="wrapper">
    <food-item    
        v-for="x in foods"
        :food-name="x.name"
        :food-desc="x.desc"
        :is-favorite="x.favorite"
    />
</div> <!--컴포넌트-->
</template>


<script>
export default{
    data(){
        return{
        foods: [
        { name: 'Apples', 
          desc: '사과는 빨개~', 
          favorite: true },
        { name: 'Pizza', 
          desc: '피자는 맛없으~', 
          favorite: false },
        { name: 'Rice', 
          desc: 'Rice is a type of grain that people like to eat.', 
          favorite: false },
        { name: 'Fish', 
          desc: '날로 먹어야지~', 
          favorite: true },
        { name: 'Cake', 
          desc: '느무 달어~', 
          favorite: false }
      ]
        }
    }
}
</script>


<style>
/* *{color:rgb(68, 43, 10);} */
#wrapper {
    display: flex;
    flex-wrap: wrap;
  }
  #wrapper > div {
    border: dashed black 1px;
    flex-basis: 120px;
    margin: 10px;
    padding: 10px;
    background-color: rgb(18, 126, 153);
  }
</style>




