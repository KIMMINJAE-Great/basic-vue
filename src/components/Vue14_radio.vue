<template>
  <h1>Radio</h1>
  Radio에서 value는 v-model로 선택되었을 때 활용됨 생략 X
  <label for="one">One</label>
  <input type="radio" name="radio" id="one" value="one1" v-model="picked"/>
  <label for="two">Two</label>
  <input type="radio" name="radio" id="two" value="two" v-model="picked"/><br>
  <span> picked:{{ picked }}</span>
</template>

<script>
export default {
  data() {
    return { picked: "asdasdas" };
  },
};
</script>

<style>
</style>