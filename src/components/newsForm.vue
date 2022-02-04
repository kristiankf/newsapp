<template>
    <form>
        <h2>NewsNews Update</h2>
        <div>
            <label for="Title">News Title:</label>
            <p><input type="text" id="Title" placeholder="News title here"></p>
        </div>
        <div>
            <label for="headline">News Headline</label>
            <p><textarea id="headline" placeholder="Headline here"></textarea></p>
        </div>
        <div>
            <input type="submit" value="Post">
        </div>
    </form>
</template>

<script>
export default {
    name: 'newsForm',
    
}
</script>

<style scoped>

</style>