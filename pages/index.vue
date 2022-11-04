<template>
  <div>
    <!-- <Header/>
    <Welcome/>
    <Popular/>
    <Free/>
    <Latest/>
    <Trending/>
    <Join/>
    <LeaderBoard/>
    <Footer/> -->
  </div>
</template>

<script>
import ENV from '@/env'
export default {
  data() {
    console.log(process.env.TEST_VARIABLE)
    console.log(ENV.google.googleApiKey1)
    console.log(ENV.google.googleApiKey2)
  }

}
</script>
