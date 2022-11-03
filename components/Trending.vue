<template>
    <div>
    <div class="inner-width">
        <div class="section-title">
          <h2>트렌딩</h2>
          <ul class="section-bar">
            <li>오늘</li>
            <li>이번 주</li>
          </ul>
        </div>
        <div class="movie-box" :style="{ background: `url(${backgroundImg}) no-repeat bottom` }">
          <div v-for="(movie, index) in movies" :key="index" class="movie">
            <NuxtLink 
              :to="{ name: 'movies-movieid', 
              params: { movieid: movie.id } }" 
              class="poster"
            >
            <img 
            :src="`https://image.tmdb.org/t/p/w500/${movie.poster_path}`"
             alt=""
             />
            <div class="movie-vote-average">
              <p>{{ movie.vote_average.toFixed(1) }}</p>
            </div>
            </NuxtLink>
          
          <div class="movie-info">
            <NuxtLink 
              :to="{ name: 'movies-movieid', 
              params: { movieid: movie.id } }" 
              class="title"
            >
              {{ movie.title }}
            </NuxtLink>
            <p class="release">
              {{
                new Date(movie.release_date).toLocaleString('en-us', 
                {
                  month: 'long',
                  day: 'numeric',
                  year: 'numeric',
                })}}
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
  </template>
  
  <script>
  import axios from 'axios'
  import backgroundImg from '../assets/imgs/trending-img.png';
  export default {
      name: 'Trending',
      data() {
    return {
      movies: [],
      backgroundImg, 
    }
  },
  async fetch() {
    await this.getMovies()
  },
  methods: {
    async getMovies() {
      const data = axios.get(
        `https://api.themoviedb.org/3/trending/all/day?api_key=dca826d7ecad36cf56d8b27692dac7ac`
      )
      const result = await data
      result.data.results.forEach((movie) => {
        this.movies.push(movie)
      })
      console.log(this.movies)
    },
  },
  }
  </script>
  
  <style lang="scss" scoped>

  </style>