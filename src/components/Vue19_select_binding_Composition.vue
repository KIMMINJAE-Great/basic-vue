<template>
  <h1>select binding Composition API</h1>
  select는 바인딩을 할 때 option의 value에 binding을 한다.<br>
  <select name="selItem" ref="selItem" id="selItem" v-model="selected" v-on:change="selChange">
    <option value="반지">ring</option>
    <option value="목걸이">necklace</option>
    <option value="귀걸이">earring</option>
    <option value="시계">watch</option>
    <option value="팔찌">bracelet</option>
  </select><br>
  <span>{{selected}} /{{selectText}}</span><br>
  <span>{{selected}} /<span ref="selText" id="selText"></span></span>
</template>

<script>
import { onMounted, ref } from '@vue/runtime-core';
export default {
  //::CompositionAPI  Vue3.x

  setup() {
    const selItem = ref(null)
    const selText = ref(null)
    const selected = '반지'  
    const selectText = ref('')// ref와 23행 ''는 용도가 다음

    //첫 화면에 select의 text를 들고 오기 위한 함수
    const getSelText= (function() {
      selChange()
    })
    
    // select 변경될 때마다 동작하는 함수
    const selChange = function(){
      selectText.value = selItem.value.options[selItem.value.selectedIndex].text;
      selText.value.textContent =selItem.value.options[selItem.value.selectedIndex].text;
    }
    
    onMounted(() =>{
      getSelText()
    })
    return {
      selItem, selText, selected, selectText, getSelText, selChange
    }
    
  }, 
}
</script>

<style>

</style>
