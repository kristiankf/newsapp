<template>
  <div id="app">
    <Header />
    <Navbar />
    <NewsForm />
    <NewsSection  :img = "image" />
    <Footer />
  </div>
</template>

<script>

import Navbar from './components/navbar.vue'
import Header from './components/appHeader.vue'
import NewsSection from './components/newsSection.vue'
import Footer from './components/footer.vue'
import NewsForm from './components/newsForm.vue'


export default {
  name: 'App',
  components: {
    Navbar,
    Header,
    NewsForm,
    NewsSection,
    Footer,
  },

  data() {
    return {
      image: './logo.png',
      news: [{
        id: 1,
        headline: 'headline',
        newContent: ''
      }]
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
