<template>
  <h1>form element join</h1>
  <form action="Vue20_memberList.vue" ref="frm">
    <fieldset>
      <legend>회원 가입!</legend>
      <div>
        <label for="id" class="title"> ID</label>
        <input type="text" ref="id" id="id" />
      </div>
      <div>
        <label for="name" class="title">Name</label>
        <input type="text" ref="name" id="name" />
      </div>
      <div>
        <label for="pass" class="title">Password</label>
        <input type="password" ref="pass" id="pass" />
      </div>
      <div>
        <label for="repass" class="title">Re Password</label>
        <input type="password" ref="repass" id="repass" />
      </div>
      <div>
        <label class="title">Hobby</label>
        <label :for="item" v-for="(item, i) in hobbyList" :key="i">
          {{ item
          }}<input
            type="checkbox"
            name="hobby"
            :id="item"
            :value="item"
            v-model="hobby"
          />
          <!-- v-for돌린것을 item들에게 -->
        </label>
      </div>
      <div>
        <label class="title">Gender</label>
        <label :for="item" v-for="(item, i) in genderList" :key="i">
          {{ item
          }}<input
            type="radio"
            name="gender"
            :id="item"
            :value="item"
            v-model="gender"
            ref="item"
          />
        </label>
      </div>
      <div>
        <label for="" class="title">Mobile</label>
        <select v-model="selected" name="mobile" id="mobile" ref="m1">
          <option v-for="(item, i) in mobileList" :value="item" :key="i">
            {{ item }}
          </option>
        </select>
        - <input type="text" class="m" id="mobile1" ref="m2" /> -
        <input type="text" id="mobile2" ref="m3" class="m" />
        <input type="hidden" name="mobile" v-model="mobile" ref="mobile" />
      </div>
      <div>
        <label class="title"></label
        ><!-- 공백-->
        <button ref="btnJoin" type="submit" @click.prevent="join" class="btn-margin">
          가입
        </button>
        <button ref="btnCancel" @click.prevent="cancel">취소</button>
      </div>
    </fieldset>
  </form>
</template>

<script>
export default {
  data: () => ({
    hobby: [],
    hobbyList: ["축구", "배구", "농구"],
    gender: "여",
    genderList: ["남", "여"],
    mobile: "선택",
    mobileList: ["010", "011", "016"],
  }),
  methods: {
    join() {
      const frm = this.$refs.frm;
      const id = this.$refs.id;
      const name = this.$refs.name;
      const pass = this.$refs.pass;
      const repass = this.$refs.repass;
      const m1 = this.$refs.m1;
      const m2 = this.$refs.m2;
      const m3 = this.$refs.m3;
      const mobile = this.$refs.mobile;
      
        if(id.value =="" || id==undefined){
          alert('ID(을)를 확인해주세요')
          return
        }
        if(name.value =="" || name==undefined){
          alert('Name(을)를 확인해주세요')
          return
        }
        if(pass.value =="" || pass==undefined){
          alert('Password(을)를 확인해주세요')
          return
        }
        if(pass.value !=repass.value ){
          alert('비밀번호(을)를 재확인해주세요')
          return
        }
        if(m1.value =="" || m1==undefined){
          alert('전화번호 010(을)를 확인해주세요')
          return
        }
        if(m2.value =="" || m2==undefined){
          alert('전화번호 앞자리 (을)를 확인해주세요')
          return
        }
        if(m3.value =="" || m3==undefined){
          alert('전화번호 뒷자리 (을)를 확인해주세요')
          return
        }
        if(mobile.value =="" || mobile==undefined){
          alert('Mobile(을)를 확인해주세요')
          return
        }

        

   
    frm.submit();
   
   },
   

   
    
   
    
    

    cancel() {
      this.$refs.frm.reset()
      document.querySelector("#여").checked = true;//단순히 document의 값을 초기화, 해당  버튼의 아이디를 querySelector에#~~
     
    },
},
    
  }

</script>

<style>
.title {
  display: inline-block;
  width: 120px;
  margin: 5px;
  text-align: left;
} /*정렬 방법*/
fieldset div {
  width: 100%;
  text-align: left;
}
.m {
  width: 50px;
}
.btn-margin {
  margin: 30px 20px;
}

/* checkForm(e) {
      e.preventDefault();
      if(id=="" || id==undefined){
          alert('ID(을)를 확인해주세요')
          return
        }
        if(name=="" || name==undefined){
          alert('Name(을)를 확인해주세요')
          return
        }
        if(pass=="" || pass==undefined){
          alert('Password(을)를 확인해주세요')
          return
        }
        if(pass!=repass){
          alert('비밀번호(을)를 재확인해주세요')
          return
        }
        if(m1=="" || m1==undefined){
          alert('전화번호 010(을)를 확인해주세요')
          return
        }
        if(m2=="" || m2==undefined){
          alert('전화번호 앞자리 (을)를 확인해주세요')
          return
        }
        if(m3=="" || m3==undefined){
          alert('전화번호 뒷자리 (을)를 확인해주세요')
          return
        }
        if(mobile=="" || mobile==undefined){
          alert('Mobile(을)를 확인해주세요')
          return
        }
    } */
</style>
