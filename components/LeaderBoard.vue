<template>
    <div>
      <div class="inner-width">
          <div class="section-title">
            <h2>리더보드</h2>
            <div class="board-list">
              <ul>
                <li class="green">All Time Edits</li>
                <li class="orange">Edits This Week</li>
              </ul>
              </div>
              <div class="person-box">
                <div v-for="(person, index) in movies" :key="index" class="person">
                  <NuxtLink 
                    :to="{ name: 'person-movieid', 
                    params: { movieid: person.id } }" 
                    class="profile"
                  >
                  <img 
                  :src="`https://image.tmdb.org/t/p/w500/${person.backdrop_path}`"
                    alt=""
                    />
                  <div class="person-name">
                    <p>{{ person.name }}</p>
                  </div>
                  </NuxtLink>
                
                  <div class="person-info">
                    <NuxtLink 
                      :to="{ name: 'people-movieid', 
                      params: { movieid: person.id } }" 
                      class="title"
                    >
                      {{ people.popularity}}
                    </NuxtLink>
                  </div>
                </div>
              </div>
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
      people: [],
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
      result.data.results.forEach((person) => {
        this.people.push(person)
      })
    },
  },
}
  </script>
  <style lang="scss" scoped>
 
  .board-list{  
    display: flex;
    flex-direction: column;
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
.person-box{
  display: flex;
  flex-direction: column;
  .person{
    width: 100%;
    .profile{
      width: 100px;
    }
  }
}
  </style>