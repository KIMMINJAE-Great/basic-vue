<template>
  <h1>Select</h1>
  select의 option에 value를 넣지 않으면 text의 값이 value가 됨<br>
  <!-- <select v-model="selected" multiple name="" id=""> -->
  <select v-model="selected" name="" id="">
    <option value="" disabled >Please Select One</option>
    <option value="1">A</option>
    <option >B</option>
    <option >C</option>
  </select>
  <span>{{selected}}</span><br>
  <select v-model="arrSelect" name="" id="">
    <option value="" disabled >Please Select One</option>
    <option v-for="(item, i) in arrObj" :key="i" :value="item.value">{{item.text}}</option>
  
  </select>
</template>


<script>
export default {
  data:()=>({
    selected : "A",
    arrSelect : ["C",'A'],
    arrObj : [{text:'One',value:'A'},{text:'Two',value:'B'},{text:'Three',value:'C'},{text:'Four',value:'D'}],
    arrSring:['A','B','C','D'],
  })
}
</script>

<style>

</style>