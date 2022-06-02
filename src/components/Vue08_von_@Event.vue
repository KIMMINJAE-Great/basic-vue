<template>
  <h1>v-on @Event</h1>
  <form action="http://127.0.0.1:8080" method="post">
  <button type="submit" @click="warning('Warning!!',$event)"> Warning</button>
  </form>
</template>

<script>
export default {
  methods : {
    //warning(){} 
    warning: function(msg, e ){ 
      //e 가 존재한다면 => $event를 통해서 native Event에 접근 가능
      if(e) e.preventDefault();
      alert(e)
      alert(msg)
      }
      
  }
}
</script>

<style>

</style>