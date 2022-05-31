<template>
  <h1>v-once</h1>
  <span v-once> 다시는 변경되지 않습니다.{{msg}}</span> <br>  <!-- msg의 내용이 v-once속성 때문에  바뀌지 않는다-->
  <span>변경이 잘 됩니다.{{msg}}</span><br>
  <input type="text" v-model="msg"/><!-- msg의 내용을 수정하는 곳-->
  
</template>

<script>
const data = {"msg":"v-once이기 때문이죵"}
export default {
  data(){
    return data
    // return { 
    //   // msg:"v-once 이기 때문이죵", 전역에 안두었을때
    // }
  }
  // data:() => ({"msg":"v-cone이기 때문이죠"})
  //기본
  //data(){ return {} }
  //화살함수
  // data:()=>{}
  //객체를 return할때 화사표
  // data : ()=>({키:값})  ()는 외부에서 참여되지 않게 막는거
}
//data.msg = '안바뀌는 것은 v-once가 아니기 때문이죠'//쓰면 오버라이딩?
</script>

<style>


</style>