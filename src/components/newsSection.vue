<template>
    <div class="news-container">
      <News v-for="news in newsDetails"
       :key='news.id' 
       :img="img" 
       :newsContent="news" 
       :showDelete="showDeleteButton" 
       @del-news="$emit('del-news', news.id)"/>
      <!-- <News :img = "img" />
      <News :img = "img" /> -->
    </div>
</template>

<script>
import News from './news.vue'

export default {
    name: 'NewsSection',
    props: ["img", "newsDetails", "showDeleteButton"],
    components: {
        News,
    }
}
</script>

<style scoped>
  .news-container {
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
      padding: 20px;
      margin: auto;
  }
  @media screen and (min-width: 1300px) {
    .news-container {
      width: 80%;
    }
  }
</style>