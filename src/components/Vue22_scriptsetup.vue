<template>
<h1>&lt;script setup&gt; tag</h1>
<h3>script setup를 이용하면 components옵션(exports deafualt(){})도 필요 없고
  setup함수를 만들 필요도 없으며, 명시적으로 변수를 반환하지 않아도 됨
</h3>
<input type="text" v-model="title" ref="msg" >
<button @click="change">바꾸기</button>
</template>

<script setup>
const {ref}=require("@vue/reactivity");

let title = ref('old title')
const msg = ref(null)  //msg는 ref로 서너언??
function change(){
  msg.value.value = "new title";  //msg의 값 anfdjqhrl  msg.value찍어보기
  console.log(msg.value);//msg.value는 <input type="text"> msg.value의 value는 text가 된다.
}
</script>
