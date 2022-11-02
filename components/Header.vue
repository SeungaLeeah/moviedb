<template>
  <div class="MF-set">
    <div class="inner-width">
      <div class="header">
      <ul class="text-container">
        <li><img class="main-logo" src="../assets/imgs/mainlogo.png" alt="mainlogo"/></li>
          <li>영화</li>
          <li>TV프로그램</li>
          <li>인물</li>
          <li>More</li>
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
}
</script>

<style lang="scss" >
.header{
display: flex;
flex-direction: row;
align-items: center;
height: 65px;
font-size: 16px;
box-sizing: border-box;
padding: 0 20px;
  .text-container{
    display: flex;
    width: 50%;
    flex-direction: row;
    align-content: center;
    
    li{
      cursor: pointer;
      padding: 0 20px;
      .main-logo{
        height: auto;
        width: 155px;
        cursor: pointer;
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
 
</style>
