<template>
  <h1>v-on Mouse Event</h1>
  <input type="button" value="마우스 왼쪽" 
  v-on:click.left="mouse_left" v-on:click.right="mouse_right" 
  v-on:click.middle="mouse_middle"
  v-on:contextmenu="mouse_right"> <br>
  <input type="text" v-on:click.meta="onMeta"><br>
  <input type="text" v-on:click.exact.alt.shift="onMixKey1"   
  v-on:click.exact="onMixKey2">
</template>

<script>
export default {
  methods:{
    mouse_left(){
      console.log("마우스 왼쪽 버튼을 눌렀어요");
    },
    mouse_right(){
      console.log("마우스 오른쪽 버튼을 눌렀어요");
    },
    mouse_middle(){
      console.log("마우스 가운데 버튼을 눌렀어요");
    },
    onMeta(){console.log("윈도우키를 누른 상태에서 좌클릭했어요");
    },
    onShift(){console.log("shift를 눌렀어요");
    },
    onMixKey1(){console.log("alt shift 좌클를 눌렀어요 ,1복합키");
    },
    onMixKey2(){console.log("좌클릭 눌렀어요,2복합키");
    },
  }
}
</script>

<style>

</style>