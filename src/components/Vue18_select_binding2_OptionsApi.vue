<template>
  <h1>select binding options API</h1>
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
export default {
  // options API 방식 :: Vue2.x  양방향  18~48행까지 
  data: ()=>({selected: '반지',selectText: ''}),
  methods: {
    selChange(e){
      const sel = e.target;
      const selText = this.$refs.selText;

      // console.log(sel.value);
      // console.log(sel.options[sel.selectedIndex].text);
      this.selectText = sel.options[sel.selectedIndex].text;
      selText.textContent =sel.options[sel.selectedIndex].text;
    },
    getSelText() {
      // ::$refs 접근 Vue 2.x  /3.x지원안됨
      // const selItem = this.$refs.selItem;
      // const selText = this.$refs.selTextt;
      // this.selectText = selItem.options[selItem.selectedIndex].text;
      // selText.textContent = selItem.options[selItem.selectedIndex].text;
      // console.log(this.selectText);

      //::dom 접근
      const selItem = document.querySelector("#selItem")
      const selText = document.querySelector("#selText")
      this.selectText = selItem.options[selItem.selectedIndex].text;
      selText.textContent = selItem.options[selItem.selectedIndex].text;
    },
  },

  mounted: function(){
    this.getSelText();
  }

}
</script>

<style>

</style>