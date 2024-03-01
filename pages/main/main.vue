<script setup>
import { onMounted } from 'vue';
    console.log('inside js ');

    const makeMap = () => {
        console.log('... map >> ');
        let container = document.getElementById('map'); //지도를 담을 영역의 DOM 레퍼런스
        let options = { //지도를 생성할 때 필요한 기본 옵션
            center: new kakao.maps.LatLng(33.450701, 126.570667), //지도의 중심좌표.
            level: 3 //지도의 레벨(확대, 축소 정도)
        };

        let map = new kakao.maps.Map(container, options); //지도 생성 및 객체 리턴
        kakao.maps.load(map);
    }

    onMounted(() => {
        console.log('inside onMounted');
        makeMap();
    })

  
</script>

<template>
    <div>
        <div id="map" style="width:100vw;height:100vh;"></div>
        
        <div class="menu-btns">
            <div class="btns-wrapper">
                <button class="btn-border active">지도</button>
                <button class="btn-border">게시판</button>
                <button class="btn-border">채팅</button>
                <button class="btn-border">내정보수정</button>
                <button class="btn-border">맛집추가</button>
            </div>
            <!-- <ul>
                <li>
                    <button class="btn-border">게시판</button>
                </li>
                <li>
                    <button class="btn-border">채팅</button>
                </li>
                <li>
                    <button class="btn-border">내정보</button>
                </li>
            </ul> -->
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