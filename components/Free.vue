<template>
    <div>
    <div class="inner-width">
        <div class="section-title">
          <h2>Free To Watch</h2>
          <ul class="section-bar">
            <li class="choice">영화</li>
            <li>TV</li>
          </ul>
        </div>
        <div class="movie-box">
          <div  v-for="(movie, index) in movies" :key="index" class="movie">
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
              <p>{{ movie.vote_average }}</p>
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
  export default {
      name: 'Free',
      data() {
    return {
      movies: [],
    }
  },
  async fetch() {
    await this.getMovies()
  },
  methods: {
      async getMovies() {
        const data = axios.get(
          `https://api.themoviedb.org/3/movie/top_rated?api_key=dca826d7ecad36cf56d8b27692dac7ac&language=en-US&page=1`
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
 
  </style>