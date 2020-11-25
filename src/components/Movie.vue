<template>
    <div class ="TopPic" align="center">
      <div class="centering_parent">
        <div v-show="!checkPassWord">
           <input v-model="password" placeholder="Enter PassWord">
        </div>
      </div>
      <div v-show="checkPassWord">
        <p class = "Body">
          旅のおもひで
        </p>
        <video src="https://tarumoto-spa.s3-ap-northeast-1.amazonaws.com/forMovie/Video.mp4" controls width="80%"></video>
      </div>
    </div>
</template>

<script>
export default {
  components: {
  },
  data: function () {
    return {
      flag: true,
      password: '',
      rightPassword: 'a19F'
    }
  },
  computed: {
    checkPassWord: function () {
      return this.password === this.rightPassword
    }
  }
}

</script>

<style>
.TopPic{
  position:absolute;
  top: 80px;
  left: 80px;
}

.centering_parent {
    text-align:  center;        /* 中央寄せ */
    height: 50px;              /* 高さ指定 */
}

.Content{
  font-family: 'Amatic SC', cursive;
  font-size: 80px;
  background-color: transparent;
  word-break: keep-all;
}

.Body{
  font-family: "Sawarabi Mincho";
  font-size: 20px;
  line-height: 150%;
}

.hr_bar {
  position: relative;
  height: 1px;
  border-width: 10;
  background-color: #00bcd4;
  background-image: -webkit-linear-gradient(left,#00bcd4 0%,#283593 50%,#00bcd4 100%);
  background-image:         linear-gradient(90deg,#00bcd4 0%,#283593 50%,#00bcd4 100%);
}

</style>
