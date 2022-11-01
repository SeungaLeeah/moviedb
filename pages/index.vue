<template>
  <div></div>
</template>

<script>
import axios from '@nuxtjs/axios';
export default {
  data() {
    return {
      moives: [],
    }
  },
  methods: {
    async getMovies() {
      const data = axios.get(
        `https://api.themoviedb.org/3/movie/now_playing?api_key=dca826d7ecad36cf56d8b27692dac7ac&language=en-US&page=1`
      )
      const result = await data
        console.log(result) 
    },
  },
}
</script>
