<template>
  <h1>form element select binding</h1>
  select는 바인딩을 할 때 option의 value에 binding을 한다.<br>
  <select name="selItem" id="selItem" v-model="selected" v-on:change="selChange">
    <option value="반지">ring</option>
    <option value="목걸이">necklace</option>
    <option value="귀걸이">earring</option>
    <option value="시계">watch</option>
    <option value="팔찌">bracelet</option>
  </select>
  <br /><span>{{ selected }}</span>
</template>

<script>

export default {
  data: () => ({
    selected: "시계",
  }),
  methods: {
    selChange(e){    // e. event selChange이벤트 발생시 e를 가져와 값을 출력
      const sel = e.target; //e.target의 난발은 좋지 않아 변수화
      console.log(sel.value);
      console.log(sel.options[sel.selectedIndex].text);  //text출력방법 options확인
    }
  },
 
};
</script>

<style>
</style>