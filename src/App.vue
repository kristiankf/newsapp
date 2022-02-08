<template>
  <div id="app">
    <Header />
    <Navbar @show-form="showForm" @show-delete-button="showDelete" />
    <NewsForm @details-submitted="addNews" 
    :newsDetails="newsDetails" v-if = 'showNewsForm' />
    <NewsSection  :img="image" :newsDetails="newsDetails" 
    :showDeleteButton="showDeleteButton"
    @del-news="deleteNews" />
    <Footer />
  </div>
</template>

<script>

import Navbar from './components/navbar.vue'
import Header from './components/appHeader.vue'
import NewsSection from './components/newsSection.vue'
import Footer from './components/footer.vue'
import NewsForm from './components/newsForm.vue'
import newsimage1 from '@/assets/newsimage1.jpg'


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
      image: newsimage1,
      showNewsForm: false,
      showDeleteButton: false,
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
      {
        title: "yes",
        id: 3,
        headline: 'haha',
        newContent: ''
      }
      ]
    }
  },
  methods: {
    addNews(newsDetails) {
      this.newsDetails.push(newsDetails)
    },
    showForm(show) {
      this.showNewsForm = show
    },
    showDelete(show) {
      this.showDeleteButton = show
    },
    deleteNews(id) {
      this.newsDetails = this.newsDetails.filter(news => news.id !== id)
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
