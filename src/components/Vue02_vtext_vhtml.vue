<template>
<h1>선언적 렌더링</h1>
  {{message}}  <!--보통크기-->
  <h3 v-text="message"></h3><!--h3크기, <a>문자로 출력--> 
  <h3 v-html="message"></h3> <!-- a태그 적용된 상태?// 태그로 button도 가능-->
</template>

<script>
export default {
  data(){
    return {message : "<a href=#> Vue3 Progaraming</a>"}
  }
}
</script>

<style>

</style>