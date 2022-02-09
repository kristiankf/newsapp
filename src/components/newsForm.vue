<template>
    <form @submit.prevent="onSubmit">
        <h2>NewsNews Update</h2>
        <div class="field">
            <label for="Title">News Title:</label>
            <p><input type="text" id="Title" 
            placeholder="News title here" v-model="title"
            required></p>
        </div>
        <div class="field">
            <label for="headline">News Headline:</label>
            <p><textarea id="headline" placeholder="Headline here"
            v-model="headline" required></textarea></p>
        </div>
        <div class="field submit">
            <input type="submit" value="Post">
        </div>
    </form>
</template>

<script>
export default {
    name: 'newsForm',
    props: ['newsDetails'],
    data() {
        return {
            title: null,
            headline: null,
        }
    },
    methods: {
        onSubmit() {
            let newsDetails = {
                id: this.idGenerator,
                title: this.title,
                headline: this.headline,
            }
            this.$emit('details-submitted', newsDetails)
            this.title= null
            this.headline=null
        }
    },
    computed: {
        idGenerator(){
            let t = true
            let id
            let idlist = []
           
            if (this.newsDetails.length == 0){
                id = 1
                return id
            }
            else {
                for (let news in this.newsDetails){
                  idlist.push(news.id)
                }
                while (t){
                    let rand = Math.floor(Math.random() * 100)
                    for (let i in idlist){
                        if (rand == idlist[i]){
                            t = true
                            break;
                        }
                        t = false
                        id = rand
                    }
                }
            return id
            }  
        },
    }
    
}
</script>

<style scoped>
  form {
      width: 40%;
      border: 1px solid green;
      margin: auto;
      margin-top: 20px;
      padding: 15px;
      /* box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.2), 
      0 3px 10px 0 rgba(0, 0, 0, 0.19); */
      /* display: none; */
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

  @media screen and (max-width: 706px) {
      form {
          width: 90%;
          
      }
  }
</style>