<template>
    <form>
        <h2>NewsNews Update</h2>
        <div class="field">
            <label for="Title">News Title:</label>
            <p><input type="text" id="Title" placeholder="News title here"></p>
        </div>
        <div class="field">
            <label for="headline">News Headline:</label>
            <p><textarea id="headline" placeholder="Headline here"></textarea></p>
        </div>
        <div class="field submit">
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
  form {
      width: 50%;
      border: 1px solid green;
      margin: auto;
      padding: 15px;
      box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.2), 
      0 3px 10px 0 rgba(0, 0, 0, 0.19);
      display: none;
  }

  input[type=text] {
      width: 100%;
      height: 40px;
      padding: 10px;
      border-radius: 5px;
      border: 1px solid green;
  }

  textarea {
      width: 100%;
      height: 80px;
      border-radius: 5px;
      padding: 10px;
      border: 1px solid green;
  }

  input[type=submit] {
      width: 50%;
      border: none;
      padding: 10px;
      color: white;
      background: green;
      border-radius: 5px;
  }

  .field {
      margin-top: 15px;
  }

  .submit {
      text-align: center;
  }

  input:focus, textarea:focus{
      border: 1px solid red;
      outline: none;
  }
</style>