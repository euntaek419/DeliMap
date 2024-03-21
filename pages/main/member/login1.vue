<template>
  <div class="container">
    <div class="wrapper">
      <div class="login-top">
        <span>DeliMap</span>
      </div>
      <div class="login-bottom">
        <div class="login-id">
          <input type="text" class="login-neccessary" placeholder="아이디">
        </div>
        <div class="login-pw">
          <input type="password" class="login-neccessary" placeholder="비밀번호">
        </div>
        <div class="login-btn">
          <button>로그인</button>
        </div>
        <div class="login-save" >
          <label for="login-chk">
            <input type="checkbox" name="keeplogin">
            <span>로그인 유지</span>
          </label>
            <a href="#" class="join">회원가입</a>
        </div>
            <div class="find">
              <a href="#" class="find-id">아이디 찾기 </a>
              <span> | </span>
              <a href="#" class="find-pw"> 비밀번호 찾기</a>
            </div>
      </div>
      <div class="kakaoLogin">
        <img src="@/pages/assets/kakao_login_medium_wide.png" alt="이미지 설명">
      </div>
    </div>
  </div>
</template>
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Ultra&display=swap');
.container {
  display: flex;
  margin: 0 auto;
  padding-top:30px;
  padding-bottom: 30px;
}
.wrapper {
  display: flex;

  margin: 0 auto;
  max-width: 330px;
  flex-direction: column;
  position: relative;
}
.login-top {
  padding:40px 0;
  color:rgb(248, 179, 60);
  text-align: center;
}
.login-top span{
  margin: 0 auto;
  font-size: 60px;
  font-family: "Ultra", serif;
  font-style: normal;
}
.login-bottom {
  flex-direction: column;
}
.login-bottom input {
  outline: none;
}
.login-id {
  margin-bottom:10px;
}
.login-neccessary {
  width: 100%;
  border-bottom:1px solid rgb(218, 218, 218);
  padding:10px;
  color: black;
  font-size: 15px;
}
.login-neccessary::placeholder {
  color: #A2A2A1;
  font-size: 14px;
}
.login-btn {
  width: 100%;
  border:1px solid rgb(247, 160, 8);
  padding: 8px;
  margin-top: 50px;
  margin-bottom: 15px;
  text-align: center;
  background-color: rgb(248, 179, 60);
  cursor: pointer;
  border-radius: 4px;
}
.login-btn button {
  font-size: 25px;
  color:white;
  text-align: center;
}
.login-save {
  margin-top: 10px;
  margin-bottom: 30px;
  display: flex;
  justify-content: space-between;

}
.login-save label {
  display: flex;
  align-items: center;
}
.join {
  text-decoration-line: none;
}
.join:link {
  color: black;
}
.join:visited {
  color: black;
}
.login-save input {
  width: 20px;
  height: 20px;
  border-radius: 10px;
  margin-right:10px;
}
.find {
  display: flex;
  justify-content: space-around;
  margin-bottom: 60px;
}
.find-id {
  font-size: 14px;
  text-decoration-line: none;
}
.find-id:link {
  color: black;
}
.find-id:visited {
  color: black;
}
.find-pw {
  font-size: 14px;
  text-decoration-line: none;
}
.find-pw:link {
  color: black;
}
.find-pw:visited {
  color: black;
}
.kakaoLogin img {
  width: 100%;
  height: 56px;
  cursor: pointer;
}
hr {
  border: 0.1px solid grey;
}
</style>
<script setup>
</script>
