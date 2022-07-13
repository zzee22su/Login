<template>
  <div>
    <form>
      <div class="mb-3">
        <label for="exampleInputEmail1" class="form-label">Email address</label>
        <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" v-model="userId">
      </div>
      <div class="mb-3">
        <label for="exampleInputPassword1" class="form-label">Password</label>
        <input type="password" class="form-control" id="exampleInputPassword1" v-model="userPw">
      </div>
      <button type="submit" class="btn btn-primary" @click="login">Login</button>
    </form>
  </div>
</template>

<script>

export default {
  name: 'login-compo',
  props: {
    msg: String
  },
  data() {
    return {
      userId: '',
      userPw: ''
    }
  },

  methods: {
    //TODO: 정규식 추가
    login() {
      //TODO: password 입력되지 않은 상태에서 버튼 클릭 시, alert 메시지 창 띄우기
      if(this.userId === '') {
        alert('e-mail을 입력해주세요.');
      }

      if(this.userPw === '') {
        alert('비밀번호를 입력해주세요.');
      }
      

    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
