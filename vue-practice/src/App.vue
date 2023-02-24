<template>
  
  <div class="menu">
    <a v-for="(a,i) in menu" :key="i"> {{ a }} </a>
    <!-- 변수작명 2개까지 가능 -왼쪽변수는 array내의 데이터 / 오른쪽변수 (i)는 1씩 증가하는 정수 자바스크립트 i숫자 느는거랑 똑같음-->

  </div>

  <div>
    {{ logo }}
    <h4 :style="color">거북스쿨 {{ products[0] }}</h4>
    <p>{{ pricel1 }}억원</p>
  </div>
  <div>
    <h4>거북스쿨 {{ products[1] }}</h4>
    <p>{{ pricel2 }}억원</p>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{

       menu : ['Home','Education', 'About', 'Profile', 'Pay'],
       pricel1 : 80,
       pricel2 : 70,
       logo : '이 회사는 얼만큼 클까?',
       color : 'color : salmon',
       products : ['5층', '6층'] //array쓰면 됨 변수 0~10시작되는거
      //변수값 저장후에 {{}}수염으로 저장 원할때 값변경 어차피 html변경되고 렌더링 알아서 됨-데이터바인딩
      //html 속성도 데이터바인딩 가능 div class="red" 이런거
    }
  },
  components: {
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.menu {

  background-color: salmon;
  padding: 15px;
  border-radius: 5px;
}

.menu a {

  color: white;
  padding: 50px;
  cursor: pointer;
}
</style>
