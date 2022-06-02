<template>
  <h1>v-on Capture Self</h1>
  <!-- <div v-on:click="doTop" id="top">
    <div v-on:click.capture="doMiddle" id="middle">
      <button type="button" @click.stop="doBottom">Bubble</button> 
      <button type="button" @click="doBottom">Bubble</button>
    </div>
  </div> -->
  stop은 자신만 이벤트를 실행할 경우 <br>
  capture는 parent가 먼저 실행해야 할 경우 자신보다 parent에 capture를 붙인다. <br>
  상위 노드에 capture가 연속적일 경우 마지막으로 적용된 노드가 먼저시작<br>
  
  <div v-on:click="doTop" id="top">
    <div v-on:click.self="doMiddle" id="middle">
      <!-- <button type="button" @click.stop="doBottom">Bubble</button> -->
      <button type="button" @click="doBottom">Bubble</button>
    </div>
  </div>
  bottom을 누르면 bottom middle top다 나와야하지만  버블링이 다 일어난다
  self는 자신이 직접 발생시킨 이벤트만 처리,
</template>

<script>
export default {
  methods: {
    doTop() {
      console.log("Top 이벤트 발생");
    },
    doMiddle() {
      console.log("Middle 이벤트 발생");
    },
    doBottom() {
      console.log("Bottom 이벤트 발생");
    },
  },
};
</script>

<style>
#top {
  width: 200px;
  height: 200px;
  background: pink;
}
#middle {
  width: 100px;
  height: 100px;
  background: greenyellow;
}
</style>