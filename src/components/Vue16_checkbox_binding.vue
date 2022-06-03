<template>

  <label for="single">
  단일 checkbox는 체크 여부에 따라 다른 상태값을 설정</label><br>
  <input type="checkbox" name="" id="single" v-model="toggle"
  v-bind:true-value="t" v-bind:false-value="f" >
  <span>{{toggle}}</span>
</template>

<script>
export default {
  data:()=>({
    toggle:'체크됨',
    t:"체크됨",
    f:"체크되지 않음",
  })
}
</script>

<style>

</style>