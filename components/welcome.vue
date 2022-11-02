<template>
  <div class="welcome-container">
    <div class="inner-width">
    <div class="background-img">
        <img src="" alt="">
    <div class="title">
    <h1>Welcome.</h1>
    <p>Millions of movies, TV shows and people to discover. Explore now.</p>
    </div>
    <div class="movie-search">
        <input type="text" placeholder="영화, TV 프로그램, 인물 검색..."  />
        <button>Search</button>
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

<style lang="scss">
.welcome-container{
    width: 100%;
    .background-img{
        background-color: gray;
        position: relative;
        width: 100%;
        height: 300px;
        .title{
            position: absolute;
        }
        .movie-search{
            position: absolute;
        }
    }
    
}
</style>