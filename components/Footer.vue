<template>
  <div class="MF-set footer-container">
    <div class="inner-width footer-box">
      <div class="footer-logo-box">
        <div class="footer-logo">
          <img src="../assets/imgs/footer.png" alt="footer-logo" class="footer-logo"/>
        </div>
          <button class="footer-btn">커뮤니티 참여</button>
        </div>
        <ul class="footer-list">
          <h4>THE BASICS</h4>
          <li>TMDb에 대해 문의하기</li>
          <li>Support Forums</li>
          <li>API</li>
          <li>System Status</li>
        </ul>
        <ul class="footer-list">
          <h4>참여하기</h4>
          <li>기여 지침서</li>
          <li>새 영화 추가</li>
          <li>새 TV 프로그램 추가</li>
        </ul>
        <ul class="footer-list">
          <h4>커뮤니티</h4>
          <li>가이드라인</li>
          <li>토론 내역</li>
          <li>기여 랭킹</li>
          <li>Twitter</li>
        </ul>
        <ul class="footer-list">
          <h4>법적 사항</h4>
          <li>서비스 이용약관</li>
          <li>API Terms of Use</li>
          <li>개인정보약관</li>
        </ul>
    </div>
  </div>
</template>

<script>
export default {
    // eslint-disable-next-line vue/no-reserved-component-names
    name: 'Footer',
}
</script>

<style lang="scss">
.footer-container{
  height: 320px;
  width: 100%;
  .footer-box{
    height: 100%;
    display: flex;
    flex-direction: row;
    justify-content: center;
    
    .footer-logo-box{
      margin-top: 40px;
      display: flex;
      flex-direction: column;
      align-items: left;
      padding: 0 20px;
      line-height: 25px;
      align-content: space-between;
    .footer-logo{
      height: 147px;
      display: flex;
      justify-content: right;
      img{
        height: 100px;
      }
    }
    .footer-btn{
        padding: 10px 30px;
        font-size: 18px;
        border-radius: 8px;
        border: none;
        color: #01b4e4;
        cursor: pointer;
      }
    }
    .footer-list{
      height: 147px;
      margin-top: 100px;
      display: flex;
      flex-direction: column;
      align-items: left;
      padding: 0 20px;
      line-height: 25px;
      h4{
        font-size: 18px;
        font-weight: 900;
      }
      li{
        cursor: pointer;
      }
    }
  }
}
</style>