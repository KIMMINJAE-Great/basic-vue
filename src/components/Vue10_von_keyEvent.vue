<template>
  <h1>v-on Key Event</h1>
  <!--<input type="submit" value="Send" v-on:keyup.enter="send">  enter로 send-->
  <input type="submit" value="Send" v-on="{'keyup.enter':send, click:send}"><br>  <!--enter click 둘다 가능-->
  <input type="text" v-on:keyup='keyPressed1($event)'><br>
  <input type="text" v-on:keyup.page-down='keyPressed2($event,"Page Down")'>
  
</template>

<script>
export default {
  
 methods:{
    send(){console.log('enter key가 눌러졌습니다.')},
    keyPressed(e) {console.log(String.fromCharCode(e.keyCode)+' is pressed');},
    keyPressed2(e, caption){console.log(caption+"("+(e.keyCode)+') is pressed')},
    }
  }

</script>

<style>

</style>