<template>
<div v-if="this.windowSize >= 800">
    <div :class="$style.TopPic" align="center">
      <img src="../assets/Profile2.jpg" width="450px" height="500px">
      <div :class="$style.Content">
        <p>Kazumasa Tarumoto</p>
        <p>1990/08/22</p>
        <p>Born in Yamaguchi</p>
      </div>
      <hr class="hr_bar" width="70%"/>
        <div class="Body">
        <p>TestDrive</p>
      </div>
    </div>
</div>
<div v-else>
  <div :class="$style.TopPic2" align="center">
    <img src="../assets/Profile2.jpg" width="300px" height="400px">
    <div :class="$style.Content">
      <p>Kazumasa Tarumoto</p>
      <p>1990/08/22</p>
      <p>Born in Yamaguchi</p>
    </div>
    <hr class="hr_bar" width="70%"/>
    <div class="Body">
      <p>TestDrive</p>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'Biograpy',
  components: {
  },
  data () {
    return {
      windowSize: 0
    }
  },
  methods: {
    handleResize: function () {
      if (window.innerWidth <= 800) {
        this.hoge = true
      } else {
        this.hoge = false
      }
    }
  },
  created () {
    this.windowSize = window.innerWidth
  }
}
</script>

<style module>
.TopPic{
  position: relative;
  margin: 5% 10% 10% 10%;
}

.TopPic2{
  position: relative;
  margin: 20% 0% 0% 0%;
}

.Content {
  font-family: 'Amatic SC', cursive;
  font-size: 80px;
  background-color: transparent;
  word-break: keep-all;
}

.Body{
  font-family: "Sawarabi Mincho";
  font-size: 30px;
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
