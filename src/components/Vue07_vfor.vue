<template>
  <h1>v-for</h1>
  <!-- <ul> -->
  <!--<li v-for="(item, idx) in list" :key="idx">{{idx+1}}. {{item}}</li>  태그 안이 아닌 사이에는 {{}}-->
  <!-- <li v-for="(item, idx) in list" :key="idx"> 2 X {{idx+1}} = {{item}} </li> -->
  <!-- <li v-for="(item, idx) in list" :key="idx">{{2}}X{{idx+1}}={{2*(idx+1)}}</li> -->

  <ul v-for="(item1, idx1) in list1" :key="idx1">
    <!-- <li v-if="item1>2" style="display:block"></li> -->
    <li v-for="(item, idx2) in list2" :key="idx2">
      {{ item1 }} X {{ idx2 + 1 }} = {{ item1 * (idx2 + 1) }}
    </li>
    
  </ul>
  <!-- </ul> -->

  <!-- for(let i =2; i<10; i++){
      for(let y=1; y<10; y++)


    }
    "i"+"*"+"y"=i*y -->
</template>

<script>
export default {
  data() {
    // return {list:['Busan','Seuol','Changwon','Pohang','Incheon']}
    // return {list:[2,4,6,8,10,12,14,16,18]}
    // return {list:[1,2,3,4,5,6,7,8,9],}
    return {
      list1: [2, 3, 4, 5, 6, 7, 8, 9],
      list2: [1, 2, 3, 4, 5, 6, 7, 8, 9],
    };
  },
};
</script>

<style>
ul li{
  display:inline;
}
</style>