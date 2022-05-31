<template>
  <div v-bind:id="dynamicId">Hello</div>
  <!-- <img v-bind:src="url + '200X100'"/> -->
  <!-- <img v-bind:src="url + '200X100'" src="./assets/logo.png/"">  src 중복 안됨 -->
  <img v-bind:src="url + '200X100'"> 
  <div v-bind:class="[classA, classB]"></div><!--변수를 복수로 넣을 때는 []-->
  <div v-bind:style="[styleA, styleB]"></div><!--도형이지만 이렇게 컴포넌트들을 활용-->
  <div :="{id:box, 'data-url':url}"></div>

</template>

<script>
export default {
  data(){    //넘겨줄 데이터
    return {
      dynamicId:"first_div",  //웹f12時 Hello의 id가 first_div가 된다
      url :"https://via.placeholder.com/",
      classA : "rect",
      classB : "fill",
      styleA : "background:green; border-radius:50px;",
      styleB : "width:100px; height:100px; border:1px solid black",
      }

  }
}
</script>

<style>
  .rect{
    width:200px; 
    height:100px;
    border:1px solid red;
  }
  .fill{
    background:blue;
  }
</style>
    