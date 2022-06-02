<template>
  <h1>V-on</h1>
  <!-- <button v-on:click="count++">Add 1</button> -->
  <button @click="count++">Add + 1</button><!-- 상기 축약형-->
  <p>위 버튼을 클릭한 횟수는 {{count}}</p>
  <!-- <input type="text" name="txt" id="txt" v-bind:value="msg" @mouseout="reverse" @mouseenter="revers"  >속성은 v-bind,,@click="reverse"-->
  <input type="text" name="txt" id="txt" v-bind:value="msg"
  v-on="{mouseout:reverse, mouseenter:reverse}" ><!-- 속성은 v-bind,,@click="reverse"-->
  <form action="http://127.0.0.1:8080" method="post">
    <input type="text" name="name" id="name" v-model="nameStr" ref="yourName"> 
    <!-- prevent, stop, once는 각각 적용가능 -->
    <button  @click.prevent.once="isName" type="submit">확인</button>
  </form>
  
</template>

<script>
export default {
  // methods:{
    //   doThis(){
      //     this.count++;
    //   }
    // }

  // data:()=>({
    //   count:0,
  //   msg: "Hello Vue3"
  // }),
    
    data(){
      return{ count:0, msg: "Hello Vue3", nameStr:""};
      },
  methods:{
      doThis(){
        this.count++;//this 중요
    },
    reverse(){
      this.msg = this.msg.split('').reverse().join('');//split으로 자르고 뒤집고 join으로 붙이고
    },
    isName(){
      // if(this.nameStr === ""){
        //   alert("name을 확인하여 주세요")
      //   return  //button의 타입이 submit이면 그냥 넘어감 
      // } 경고창 띄우기 유효성검사
      
      
      //focus()
        const name = this.$refs.yourName;
      if(name.value == ""){
        alert("name을 확인하여 주세요"),
        name.focus()
        return 
      }
    }
  }
}

       
      
    
</script>

<style>

</style>