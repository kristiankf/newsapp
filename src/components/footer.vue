<template>
    <div class="footer">
        <div class="info">
            <p class="icons">
                <a href="#" class="fa fa-facebook"></a>
                <a href="#" class="fa fa-instagram"></a>
                <a href="#" class="fa fa-twitter"></a>
            </p>
            <p class="info1"><a href="#">Info</a><a href="#">Support</a><a href="#">Marketing</a></p>
            <p class="info1"><a href="#">Terms of Use</a> <a href="#">Privacy Policy</a></p>
            <p class="copyright"> &copy; 2022 NewsNews </p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Footer',
}
</script>

<style scoped>
  .info {
      background: #333;
      font-size: 14px;
      color: whitesmoke;
      height: 300px;
      display: flex;
      /* background: green; */
      margin: auto;
      flex-direction: column;
      justify-content: center;
      align-items: center;
  }
  .fa{
      font-size: 16px;
      color: #333;
      padding: 10px;
      text-decoration: none;
      margin: 10px 5px;
      border-radius: 50%;
      background: whitesmoke;
      transition: .2s;
  }
  .info1 a{
      padding: 5px;
      text-decoration: none;
      color: whitesmoke;
      transition: .3s;
  }

  .copyright{
      padding: 10px;
      font-size: 11px;
      color: #888;
  }
  .info1 a:hover{
      color: red;
  }
  .fa-facebook:hover{
      background: rgb(66, 103, 178);
      color: whitesmoke;
  }
  .fa-twitter:hover{
      background: rgb(29, 161, 242);
      color: whitesmoke;
  }
  .fa-instagram:hover{
      background: rgb(131, 58, 180);
      color: whitesmoke;
  }
</style>