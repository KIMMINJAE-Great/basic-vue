<template>
  <h1>Form Element Binding</h1>
  <form action="">
    <input placeholder="edit me" v-model="message">
    <p>Message is {{message}}</p>
    <label for="checkbox">체크 유무:{{state}}</label>   <!-- 체크시 문구변화-->
    <input type="checkbox" id="checkbox" v-model="checked" v-on:change="checkIt"><br>
    
    <label for="banana">바나나</label> 
    <input type="checkbox" id="banana" v-model="selFruit" value="banana" name="fruits"><br>
    <label for="apple">사과</label>   
    <input type="checkbox" id="apple" v-model="selFruit" value="apple" name="fruits"><br>
    <label for="pineapple">파인애플</label>   
    <input type="checkbox" id="pineapple" v-model="selFruit" value="pineapple" name="fruits"><br>

    <span>Multiline message : </span>
    <p style="white-space: preline">{{multiline}}</p>
    <textarea v-model="multiline" cols="30" rows="10"></textarea>
    <!-- <textarea cols="30" rows="10">{{message}}</textarea>texta안에 {{}}안됨 -->
  </form>
</template>


<script>
export default {
  // data:()=>({
  //   message:"누구인가",
  //   powr:123,
  // })
  data(){
    return{
      message : '누구인가?',
      multiline : '여러 줄을 작성합니다.\n\n' ,  // \n개행
      // checked: false, // 항상 비어있게
      checked : true,
      state:'동의함',
      selFruit:['banana','pineapple'],//변수에 같은 id면 true?  
    }
  },
  methods:{
    checkIt(){
      this.state = (this.checked)?"동의함":"동의 안함"
    }
  }

}
</script>

<style>

</style>