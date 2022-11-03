<template>
    <div>
      <div class="inner-width">
          <div class="leader-title">
            
            <h2 class="leader-title">리더보드</h2>
            <div class="board-list">
              <ul>
                <li class="green">All Time Edits</li>
                <li class="orange">Edits This Week</li>
              </ul>
              </div>
              <ul class="person-container">
                <li>
                  <span class="avatar">
                    <span class="circle"><p style="background-color:#01b4e4">R</p> </span>
                    <div>
                      <div>
                        <h4>rqphqel</h4>
                        <div class="line1">
                          <div class="line-bar1" ></div>
                          <h4>62187</h4>
                        </div>
                        <div class="line2">
                          <div class="line-bar2"></div>
                          <h4>33661</h4>
                        </div>
                      </div>
                    </div>
                  </span>
                </li>
                <li>
                  <span class="avatar">
                    <span class="circle"><p style="background-color:#D29001">R</p></span>
                    <div>
                      <div>
                        <h4>RuiZafon</h4>
                        <div class="line1">
                          <div class="line-bar1"></div>
                          <h4>83007</h4>
                        </div>
                        <div class="line2">
                          <div class="line-bar2"></div>
                          <h4>8032</h4>
                        </div>
                      </div>
                    </div>
                  </span>
                </li>
                <li>
                  <span class="avatar">
                    <span class="circle"><img src="../assets/imgs/3.png" alt=""></span>
                    <div>
                      <div>
                        <h4>buszmen201 (Jarek)</h4>
                        <div class="line1">
                          <div class="line-bar1"></div>
                          <h4>7741</h4>
                        </div>
                        <div class="line2">
                          <div class="line-bar2"></div>
                          <h4>15190</h4>
                        </div>
                      </div>
                    </div>
                  </span>
                </li>
                <li>
                  <span class="avatar">
                    <span class="circle"><img src="../assets/imgs/4.jpg" alt=""></span>
                    <div>
                      <div>
                        <h4>talestalker</h4>
                        <div class="line1">
                          <div class="line-bar1"></div>
                          <h4>827830</h4>
                        </div>
                        <div class="line2">
                          <div class="line-bar2"></div>
                          <h4>5610</h4>
                        </div>
                      </div>
                    </div>
                  </span>
                </li>
                <li>
                  <span class="avatar">
                    <span class="circle"><p style="background-color:#EA148C">A</p></span>
                    <div>
                      <div>
                        <h4>arezola</h4>
                        <div class="line1">
                          <div class="line-bar1"></div>
                          <h4>34526</h4>
                        </div>
                        <div class="line2">
                          <div class="line-bar2"></div>
                          <h4>5328</h4>
                        </div>
                      </div>
                    </div>
                  </span>
                </li>
                <li>
                  <span class="avatar">
                    <span class="circle"><img src="../assets/imgs/5.jpg" alt=""></span>
                    <div>
                      <div>
                        <h4>raze464</h4>
                        <div class="line1">
                          <div class="line-bar1"></div>
                          <h4>451921</h4>
                        </div>
                        <div class="line2">
                          <div class="line-bar2"></div>
                          <h4>4635</h4>
                        </div>
                      </div>
                    </div>
                  </span>
                </li>
                <li>
                  <span class="avatar">
                    <span class="circle"><p style="background-color:#0177D2">P</p></span>
                    <div>
                      <div>
                        <h4>pingu51</h4>
                        <div class="line1">
                          <div class="line-bar1"></div>
                          <h4>381412</h4>
                        </div>
                        <div class="line2">
                          <div class="line-bar2"></div>
                          <h4>4513</h4>
                        </div>
                      </div>
                    </div>
                  </span>
                </li>
                <li>
                  <span class="avatar">
                    <span class="circle"><p style="background-color:#01B4E4">L</p></span>
                    <div>
                      <div>
                        <h4>lo_enz</h4>
                        <div class="line1">
                          <div class="line-bar1"></div>
                          <h4>13329</h4>
                        </div>
                        <div class="line2">
                          <div class="line-bar2"></div>
                          <h4>4415</h4>
                        </div>
                      </div>
                    </div>
                  </span>
                </li>
                <li>
                  <span class="avatar">
                    <span class="circle"><img src="../assets/imgs/9.jpg" alt=""></span>
                    <div>
                      <div>
                        <h4>Sheigutn</h4>
                        <div class="line1">
                          <div class="line-bar1"></div>
                          <h4>345278</h4>
                        </div>
                        <div class="line2">
                          <div class="line-bar2"></div>
                          <h4>3873</h4>
                        </div>
                      </div>
                    </div>
                  </span>
                </li>
                <li>
                  <span class="avatar">
                    <span class="circle"><p style="background-color:#D27701">K</p></span>
                    <div>
                      <div>
                        <h4>Kosel</h4>
                        <div class="line1">
                          <div class="line-bar1"></div>
                          <h4>22995</h4>
                        </div>
                        <div class="line2">
                          <div class="line-bar2"></div>
                          <h4>3768</h4>
                        </div>
                      </div>
                    </div>
                  </span>
                </li>
              </ul>
              </div>
            </div>
    </div>
  </template>
  
  <script>
 import axios from 'axios'
 
  export default {
      name: 'LeaderBoard',
      data() {
    return {
      movies: [],
    }
  },
  async fetch() {
    await this.getPeople()
  },
  methods: {
    async getPeople() {
      const data = axios.get(
        `https://api.themoviedb.org/3/person/popular?api_key=dca826d7ecad36cf56d8b27692dac7ac&language=en-US&page=1`
      )
      const result = await data
      result.data.results.forEach((movie) => {
        this.movies.push(movie)
      })
    },
  },
}
  </script>
  <style lang="scss" scoped>
 .leader-title{
    display: flex;
    flex-direction:column;
    padding: 30px;
    box-sizing: border-box;
    position: relative;
    height: 500px;
  .leader-title{
    margin: 0;
    padding: 0;
  
  }
  .board-list{  
    display: flex;
    flex-direction: row;
    width: 80%;

    ul {
    margin-left: 30px;
    list-style: none;
    font-size: 14px;
    font-weight: 300;
  }

  .green::before {
    content: "\2022";
    color: #90cea1;
    font-weight: bold;
    display: inline-block; 
    width: 1em;
    margin-left: -1em;
  }
  .orange::before {
    content: "\2022";
    color: #ff5f02;
    font-weight: bold;
    display: inline-block; 
    width: 1em;
    margin-left: -1em;
  }
}
.person-container{
  flex-wrap: wrap;
  display: flex;
  width: inherit;
  li{
    width:50%;
    display: flex;
    justify-content: left;
    align-content: center;
    padding: 5px 0;
    .avatar{
      display: flex;
    .circle{
      margin: 0;
      padding: 0;
      
      p{
      width: 60px;
      height: 60px; 
      border-radius: 70%;
      overflow: hidden;  
      color: white;
      font-size: 20px;
      font-weight: 700;
      display: flex;
      align-items: center;
      align-content: center;
      justify-content: center;
      }
        img{
          width: 60px;
          height: 60px; 
          border-radius: 70%;
          overflow: hidden;
        
        }
    }
    .line1{
      width: 100%;
      height:25px;
      display: flex;
      align-items: center;
      align-content: center;
      .line-bar1{
        width: 100%;
        height: 15px;
        display: flex;
        align-items: center;
        align-content: center;
        background: linear-gradient(to right, #90cea1 0%, #90cea1 100%);
      }
    }
    .line2{
      width: 100%;
      height: 10px;
      display: flex;
      align-items: center;
      align-content: center;
        .line-bar2{
          width: 100%;
          height: 15px;
          display: flex;
          align-items: center;
          align-content: center;
          background: linear-gradient(to right, #ff5f02 0%, #ff5f02 100%);
        }
    }
  }
  }
}
}
  </style>