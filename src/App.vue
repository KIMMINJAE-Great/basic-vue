<template>
  <img alt="Vue logo" src="./assets/logo.png">
<<<<<<< HEAD
  <h1>Vue 3 Exercise</h1>
  <hr>
  
  <div v-bind:class="classCard" v-for="(component,i) in arrList" :key="i">
    <span v-text="i+1"></span>번.<br>
  <component v-bind:is="component"></component>
</div>

<Footer :class="classFooter" msg="Footer for Your Vue.js App"/>

</template>

<script>
import Exercise01 from './components/Vue01_data.vue'
import Exercise02 from './components/Vue02_vtext_vhtml.vue'
import Exercise03 from './components/Vue03_vbind.vue'
import Exercise04 from './components/Vue04_vonce.vue'
import Exercise05 from './components/Vue05_vshow.vue'
import Exercise06 from './components/Vue06_vif.vue'
import Exercise07 from './components/Vue07_vfor.vue'
import Exercise08 from "./components/Vue08_von.vue"
import Exercise09 from "./components/Vue09_von_event.vue"
import Exercise10 from "./components/Vue10_von_keyEvent.vue"
import Exercise11 from "./components/Vue11_von_mouseEvent.vue"
import Exercise12 from "./components/Vue12_von_capture_self.vue"
import Exercise13 from "./components/Vue13_checkbox.vue"
import Exercise14 from "./components/Vue14_radio.vue"
import Exercise15 from "./components/Vue15_select.vue"
import Exercise16 from "./components/Vue16_checkbox_binding.vue"
import Exercise17 from "./components/Vue17_radio_binding.vue"
import Exercise18 from "./components/Vue18_select_binding.vue"
import Exercise19 from "./components/Vue19_form_element_join.vue"

import Footer from "./components/Vue_Footer.vue"
=======
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
import Exercise from './components/Vue10_von_keyEvent.vue'
// import Exercise from './components/Vue11_von_mouseEvent.vue'
// import Exercise from './components/Vue10_von_keyEventTeacher.vue'
// import Exercise from './components/Vue12_von_capture_self.vue'
  // import Exercise from './components/Vue13_form_element.vue'
>>>>>>> d860caa83e1b0c1f63d1ea3199ed97c50a635f20

export default {
  name: 'App',
  components: {
<<<<<<< HEAD
  Exercise01, Exercise02,Exercise03, Exercise04,Exercise05, Exercise06,
    Exercise07, Exercise08,Exercise09, Exercise10,Exercise11, Exercise12,
    Exercise13, Exercise14, Exercise15, Exercise16,Exercise17,Exercise18,
    Exercise19,

    Footer,
    },
    data(){
    return{
      arrList: [
        Exercise01, Exercise02,Exercise03, Exercise04,Exercise05, Exercise06,
        Exercise07, Exercise08,Exercise09, Exercise10,Exercise11, Exercise12,
        Exercise13, Exercise14,Exercise15, Exercise16, Exercise17,Exercise18,
        Exercise19,
      ],
      classCard:"card",
      classFooter:"footer",
    }
=======
    Exercise, Exercise2//Exercise2 //복수로 component 사용, 주석화 된거 확인
>>>>>>> d860caa83e1b0c1f63d1ea3199ed97c50a635f20
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.card{
 border: 1px solid black;float:left;
 margin-top:50px;
 margin-left:100px;
 margin-bottom:10px;
  width: 500px; height: 400px; overflow: auto;
  overflow-y: 10px;
  position: static;
  border-radius: 30px;
}
.footer{
  height:100px;margin: 0;background-color: rgb(220, 220, 220);
  line-height: 90px;padding-left: 50px; font-weight: bold;
  text-align: left; clear:both;
}
</style>
