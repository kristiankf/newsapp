<template>
  <div id="app">
    <Header />
    <Navbar />
    <NewsSection  :img = "image" />
  </div>
</template>

<script>

import Navbar from './components/navbar.vue'
import Header from './components/appHeader.vue'
import NewsSection from './components/newsSection.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    Header,
    NewsSection,
  },

  data() {
    return {
      image: './logo.png',
    }
  }
}
</script>
  
<style>
  * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      /* font-family: Arial, Helvetica, sans-serif; */
      line-height: 1.4;
      background: whitesmoke;
    }
</style>
