<template>
  <div id="app">
    <Header />
    <Navbar />
    <NewsForm @details-submitted="addNews" :newsDetails="newsDetails"/>
    <NewsSection  :img="image" :newsDetails="newsDetails"/>
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
      newsDetails: [{
        title: 'News 1',
        id: 1,
        headline: 'headline',
        newContent: ''
      },
      {
        title: 'News 2',
        id: 2,
        headline: 'haha',
        newcontent: ''
      },
      // {
      //   id: 3,
      //   headline: 'haha',
      //   newContent: ''
      // }
      ]
    }
  },
  methods: {
    addNews(newsDetails) {
      this.newsDetails.push(newsDetails)
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
