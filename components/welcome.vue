<template>
  <div class="welcome-container">
    <div class="inner-width">
    <div class="background-img">
    <div class="title">
    <h1>Welcome.</h1>
    <p>Millions of movies, TV shows and people to discover. Explore now.</p>
    </div>
    <div class="movie-search">
        <input  class="search-box" type="text" placeholder="영화, TV 프로그램, 인물 검색..."  />
        <button class="search-btn">Search</button>
    </div>
</div>
  </div>
</div>
</template>

<script>
export default {
    name: 'Welcome',
}
</script>

<style lang="scss" >
.welcome-container{
    width: 100%;
    .background-img{
        background: url(../assets/imgs/welcome.jpg) no-repeat  ;
        background-size: cover;
        position: relative;
        width: 100%;
        height: 300px;
        .title{
            position: absolute;
            left: 40px;
            top: 70px;
            line-height: 50px;
            color: white;
            h1{
                font-size: 45px;
            }
            p{
                font-size: 25px;
                font-weight: 500;
            }
        }
        .movie-search{
            width:100%;
            position: absolute;
            left: 40px;
            bottom: 50px;
            display: flex;
            .search-box{
                height: 45px;
                border-radius: 25px;
                border: none;
                box-sizing: border-box;
                padding-left: 20px;
                width: 90%;
                font-size: 18px;
                font-weight: 100;
            }
            .search-btn{
                height: 45px;
                border-radius: 25px;
                border: none;
                box-sizing: border-box;
                padding: 0 30px;
                margin-left: -45px;
                text-align: center;
                font-weight: bold;
                color: white;
                background: linear-gradient(70deg, #90cea1, #01b4e4);
                &:hover{
                    color: #0d253f;
                    cursor: pointer;
                }
            }
        }
    }
    
}
</style>