<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <Exercise msg="Welcome to Your Vue.js App"/>
  <Exercise2 msg="Welcome to Your Vue.js App"/>
  <!-- <Exercise2 msg="Welcome to Your Vue.js App"/> -->
</template>

<script>
// import Exercise from './components/Vue01_data.vue'
import Exercise2 from './components/Vue02_declaritive_rendering.vue'
// import Exercise from './components/Vue03_vbind.vue'
// import Exercise2 from './components/Vue03_vbind.vue'
// import Exercise from './components/Vue04_vonce.vue'
// import Exercise from './components/Vue05_vshow.vue'
// import Exercise from './components/Vue06_vif.vue'
// import Exercise from './components/Vue07_vfor.vue'
// import Exercise from './components/Vue08_von.vue'
// import Exercise from './components/Vue08_von_keyEvent.vue'
// import Exercise from './components/Vue09_von_event.vue'
// import Exercise from './components/Vue10_von_keyEvent.vue'
// import Exercise from './components/Vue11_von_mouseEvent.vue'
// import Exercise from './components/Vue10_von_keyEventTeacher.vue'
// import Exercise from './components/Vue12_von_capture_self.vue'
  import Exercise from './components/Vue13_form_element.vue'

export default {
  name: 'App',
  components: {
    Exercise, Exercise2//Exercise2 //복수로 component 사용, 주석화 된거 확인
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
