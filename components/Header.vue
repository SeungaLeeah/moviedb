<template>
  <div class="MF-set">
    <div class="inner-width">
      <div class="header">
      <ul class="text-container">
        <li><img class="mainLogo" src="../assets/imgs/mainlogo.png" alt="mainlogo"/></li>
          <li
            @:mouseover="mouseover"
            @:mouseleave="mouseleave"
          >
            영화
            
          <ul class=" dropdown" :class="{ isOpen }">
            <li>인기</li>
            <li>현재 상영 중</li>
            <li>개봉 예정</li>
            <li>높은 평점</li>
          </ul>
          </li>
          <li  
            @:mouseover="mouseover"
            @:mouseleave="mouseleave"
          >
            TV프로그램
            <ul class=" dropdown" :class="{ isOpen }">
              <li>인기</li>
              <li>오늘 방영</li>
              <li>TV 방영 중</li>
              <li>높은 평점</li>
            </ul>
          </li>
          <li
            @:mouseover="mouseover"
            @:mouseleave="mouseleave"
          >
          인물
            <ul class=" dropdown" :class="{ isOpen }">
              <li>인기 인물</li>
            </ul>
          </li>
          <li
            @:mouseover="mouseover"
            @:mouseleave="mouseleave"
          >
            More
            <ul class=" dropdown" :class="{ isOpen }">
              <li>토론 내역</li>
              <li>기여 랭킹</li>
              <li>지원</li>
              <li>API</li>
            </ul>
          </li>
      </ul>
      <ul class="custom-right">
          <li><font-awesome-icon icon="fa-solid fa-plus" class="iconB"/></li>
          <li><a href="" class="language">KO</a></li>
          <li>로그인</li>
          <li>회원가입</li>
          <li class="light-blue"><font-awesome-icon icon="fa-solid fa-magnifying-glass" class="iconB"/></li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    // eslint-disable-next-line vue/multi-word-component-names, vue/no-reserved-component-names
    name: 'Header',
    data :function() {
      return {
            show: true
      };
    },
    methods:{
        toggleShow(){
            this.show = !this.show;
        }
    }
}
</script>

<style lang="scss">
.header{
display: flex;
flex-direction: row;
align-items: center;
height: 65px;
font-size: 16px;
box-sizing: border-box;
padding: 0 20px;
  .text-container{
    position: relative;
    display: flex;
    width: 50%;
    flex-direction: row;
    align-content: center;
    
    li{
      cursor: pointer;
      padding: 0 20px;
      .mainLogo{
        height: auto;
        width: 155px;
        cursor: pointer;
      } 
      .dropdown{
        position: absolute;
        top: 100%;
        left: 0;
        display: none;
        padding: 0;
        list-style-type: none;
        background-color: #007db9;
          li {
          width: 250px;
          border-bottom: 1px solid #fff;
          display: block;
          padding: 10px;
          color: #fff;
          text-decoration: none;
          }
      }

    }
  }
    .custom-right{
        width: 50%;
        display: flex;
        flex-direction: row;
        justify-content: right;
      li{
        display: flex;
        padding: 0 20px;
        cursor: pointer;
       
      }
    }
  }

.iconB{
        font-size: 20px;
        
}
.language{
  border-radius: 3px;
  border: 1px solid white;
  box-sizing: border-box;
  padding: 0 3px;
  font-size: 14px;
  &:hover{
    background-color: white;
    color: #0d253f;
  }
}
.notShown {
  visibility: hidden !important;
}
</style>
