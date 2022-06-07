<!--<template>
  <h1>Diffrence Composition API and Options API</h1>
  <button @click="count++">count is :{{count}}</button>
</template>


<script>

 export default {
  
   data(){
    return{
       count:0
       }
   }
 }
 </script>-->

<!-- <template>
  <h1>OPtions API data Methods</h1>
  <button @click="addOne">Add</button>
  <span ref="result">count is: {{count}}</span>
</template>

<script>
export default {
  
   data(){
    return{
       count:0
       }
   },

   methods:{
     addOne : function(){
      //  ++this.count//return의 count 아래행에서 ++해줄거임
       this.$refs.result.textContent = `count is : ${++this.count}`//ref가 result인 태그의 택스트를 후기로 하라
     }
   }
 }
</script>-->


<!-- <template>
  <h1>Composition API ref </h1>
  <button @click="addOne">Add</button>
  <span ref="result">count is: {{count}}</span>
</template>

<script>
import { ref } from '@vue/reactivity'
export default {
  setup(){
    // options로 따지면 state의 data
    const count = ref(0) //count변수를 0이라고 초기값을 줌

    //ref
    const result = ref(null)//span태그를 초기화, 입력양식태그는 null로 초기화 한다.
    //methods
    function addOne(){
      result.value.textContent = `count is : ${++count.value}`//result는 ref타입 고로 객체 고로 .사용
    }

    
    return {
      count ,result, addOne
      }
  },
 }
</script> -->


<template>
  <h1>Composition API reactive </h1>
  <button @click="addOne">Add</button>
  <span ref="result"></span>
</template>

<script>
import { reactive, ref } from '@vue/reactivity'
export default {
  setup(){
    //복수개의 변수를 하나의 변수로 리턴하고자 할 때
    const state = reactive({
      // count :0,
      count :ref(0),  //객체 키:값
    })
    
    const result = ref(null)
    
    function addOne(){
      result.value.textContent = `count is : ${++state.count}`
    }
    
    return {
      state ,result, addOne
      }
  },
 }
</script>
