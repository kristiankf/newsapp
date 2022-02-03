<template>
    <header class="header-banner">
      <div class="banner-title"> 
        
        <h1> {{ newsTitle }} </h1>
    
      </div>
    </header>
</template>

<script>
export default {
    name: "Header",
    data() {
        return {
            newsTitle: "NewsNews"
        }
    }
}
</script>

<style scoped>
  .header-banner {
    position: relative;
    background: white;
    height: 350px;
    text-align: center;
    font-weight: bolder;
}

.banner-title {
    position: absolute;
    top: 35%;
    width: 100%;
    text-align: center;
    font-size: 30px;
}
</style>