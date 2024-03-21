<script setup>
import login1 from './member/login1.vue'

const router = useRouter()
const goLogin = () => {
    router.addRoute({ name: 'login1', path: '/login1', component: login1 });
    router.push('/login1')
}
</script>

<template>
    <div>
        <div class="menu-btns">
            <div class="btns-wrapper">
                <button class="btn-border active">지도</button>
                <button class="btn-border">게시판</button>
                <button class="btn-border">채팅</button>
                <button class="btn-border">내정보수정</button>
                <button class="btn-border">맛집추가</button>
                <button class="btn-border" @click="goLogin">로그인(임시)</button>
            </div>
        </div>
    </div>
</template>

<style scoped>
.menu-btns {
    position: absolute;
    top:20px;
    right:100px;
    z-index:99999;
}
.menu-btns .active{
    color: white;
    background-color:LightSkyBlue;
}
.menu-btns .btns-wrapper {
    display: flex;
    background: white;
    /* padding:10px; */
    box-shadow: 0px 0px 5px #444;
    border-radius: 10px;
    padding:5px;
}
.menu-btns ul li{
    margin-left: 20px;
}
.btn-border {
    /* box-shadow: 0px 0px 5px #444; */
    padding:10px;
    border-radius: 10px;
}
</style>