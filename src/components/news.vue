<template>

    <div class="news">
        <button class="delete" v-if="showDelete" @click="$emit('del-news')">x</button>
        <div class="imagecontainer">
            <a href="#">
                <img :src="img" alt="News Image">
            </a>    
        </div>
        <div class="headline">
          <a href="#"> {{ newsSnippet }}</a>
        </div>
    </div>
</template>

<script>
export default {
    name: 'News',
    props: ["img", "newsContent", "showDelete"],
    data() {
        return {
            news: "Lorem ipsum dolor sit amet, \
            consectetur adipisicing elit. Accusantium\
             dolor necessitatibus amet inventore.\
              Voluptatem incidunt harum reiciendis \
              aperiam doloribus assumendalskjljdlfjl lksjdlfjs ljdflkjs dlfjslkdj lskdjlf sdkjfls kdf",
        }
    },
    computed: {
        newsSnippet() {
            return this.newsContent.title + ": " + this.newsContent.headline
        }
    }
}
</script>

<style scoped>
  .news {
      padding: 10px;
      background: #fff;
      margin: 10px 10px;
      box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 
      0 6px 20px 0 rgba(0, 0, 0, 0.19);
      overflow: hidden;
      text-overflow: ellipsis;
      word-break: break-all;
      flex: 47%;
      position: relative;
  }

  .delete {
      border-radius: 50%;
      color: white;
      width: 25px;
      height: 25px;
      border: none;
      position: absolute;
      top: 5px;
      right: 5px;
      background: red;
      cursor: pointer;
  }

  .delete:active {
      background: rgb(240, 131, 131);
  }

  .imagecontainer {
      text-align: center;
      height: 350px;
  }

  .imagecontainer img {
      width: 90%;
      height: 90%;
      transition: .4s ease-in-out;
  }
  .headline {
      /* height: 350px; */
      font-weight: 700;
      font-family: Garamond, serif;
  }

  .news:hover img {
      width: 100%;
      height: 100%;
  }

  .news a {
      text-decoration: none;
      color: black;
  }

  .news:active {
      box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.3), 
      0 6px 20px 0 rgba(0, 0, 0, 0.3);
      color: black;
  }
  
</style>