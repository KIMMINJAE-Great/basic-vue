<template>
  <h1>Form Element</h1>
  <form action="">
    <input placeholder="edit me" v-model="message">
    <p>Message is {{message}}</p>
  </form>
</template>

<script>
export default {
  // data:()=>({
  //   message:"누구인가",
  //   powr:123,
  // })
  data(){
    return{message : '누구인가?'}
  }
}
</script>

<style>

</style>