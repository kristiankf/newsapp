<template>
    <div class="news-container">
      <News :img = "img" />
      <News :img = "img"/>
      <News :img = "img"/>
    </div>
</template>

<script>
import News from './news.vue'

export default {
    name: 'NewsSection',
    props: ["img"],
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
  }
</style>