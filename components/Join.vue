<template>
    <div>
      <div class="inner-width">
        <div class="join-image">
          <div class="join-info">
            <h2>Join Today</h2>
            <p><b>Get access to maintain your own</b> custom personal lists, 
              track what you've seen <b>and search and filter for</b> what to watch 
              next<b>—regardless if it's in theatres, on TV or available on popular 
              streaming services like Netflix, Amazon Prime Video, Disney Plus, 
              and wave.</b></p>
            <button class="signUp">Sign Up</button>
          </div>
          <ul class="join-list">
            <li>Enjoy TMDB ad free</li>
            <li>Maintain a personal watchlist</li>
            <li>Filter by your subscribed streaming services and find something to watch</li>
            <li>Log the movies and TV shows you've seen</li>
            <li>Build custom lists</li>
            <li>Contribute to and improve our database</li>
          </ul>
      </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
      name: 'Join',
  }
  </script>
  
  <style lang="scss" scoped>
  .join-image{
    background: url(../assets/imgs/join.jpg) no-repeat center ;
    background-size: cover;
    position: relative;
    width: 100%;
    height: 280px;
    color: white;
    display: flex;
    flex-direction: row;
        .join-info{
          width: 55%;
          position: absolute;
          left: 40px;
          top: 20px;
          h2{
            font-size: 30px;
            line-height: 80px;
          }
          p{
            font-size: 16px;
            font-weight: 200;
            b{
              font-weight: 500;
            }
          }
          .signUp{
            margin-top: 30px;
            background-color: #805BE7;
            border: none;
            border-radius: 6px;
            color: white;
            padding: 10px 20px;
            font-size: 16px;
            font-weight: 700;
            cursor: pointer;
          }
        }
        .join-list{
          position: absolute;
          right: 30px;
          top: 110px;
          width: 35%;
          li{
            list-style: disc;
            font-size: 14px;
            font-weight: 100;
          }
        }
  }
  </style>