<template>
  <div class="footBack footBackQian">
    <div class="footer-img" />
    <div class="fcontainer">
      <p>
        博客已萌萌哒运行
        <span>{{ longTime }}</span>
      </p>
      <p>
        
        <span class="timeJump">魔理沙は大変なものを盗んでいきました(ᗜˬᗜ)</span>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Foot',
  data() {
    return {
      longTime: 0
    }
  },
  mounted() {
    this.runTime()
  },
  methods: {
    runTime() {
      // 运行倒计时
      var oldTime = new Date('2023/04/07 00:00:00')
      setInterval(() => {
        const nowTime = new Date()
        const longTime = nowTime - oldTime
        const days = parseInt(longTime / 1000 / 60 / 60 / 24, 10) // 计算剩余的天数
        const hours = parseInt((longTime / 1000 / 60 / 60) % 24, 10) // 计算剩余的小时
        const minutes = parseInt((longTime / 1000 / 60) % 60, 10) // 计算剩余的分钟
        const seconds = parseInt((longTime / 1000) % 60, 10) // 计算剩余的秒数
        this.longTime =
          days + '天' + hours + '小时' + minutes + '分' + seconds + '秒'
      }, 1000)
    }
  }
}
</script>

<style scoped lang="less">
.footBack {
  color: #888;
  margin-top: -10px;
  font-size: 12px;
  line-height: 1.5;
  text-align: center;
  width: 100%;
  min-height: 50px;
  // margin-top: -100px;
  position: relative;
  // position: absolute;
  /*min-height: 368px;*/
}
.footBack .fcontainer {
  width: 100%;
  background: #232323;
  /*top:294px;*/
  /*left:0;*/
  /*position: absolute;*/
  padding: 15px 10px 10px 10px;
  box-sizing: border-box;
  /*z-index: 1;*/
  width: 100% !important;
}
.footBack .footer-img {
  height: 368px;
  z-index: 1;
  position: relative;
  width: 100%;
  bottom: -74px;
  pointer-events: none;
  background: url('./../../assets/img/footer01.png') no-repeat 50%;
}

.footBack p {
  margin: 5px 0;
  z-index: 3;
}
.footBack a {
  color: #795548;
  z-index: 3;
}
.footBack a:hover {
  color: #000;
}
/*心脏呼吸*/
.footBack .fheart {
  width: 25px;
  height: 25px;
  margin-top: -10px;
  top: 5px;
  position: relative;
  /*padding-top:0px;*/
  vertical-align: baseline;
  -webkit-animation: heartScale 1.33s ease-in-out infinite;
  animation: heartScale 1.33s ease-in-out infinite;
}
@keyframes heartScale {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(0.8);
  }
  100% {
    transform: scale(1);
  }
}
@-webkit-keyframes heartScale {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(0.8);
  }
  100% {
    transform: scale(1);
  }
}
/*时间跳动*/
.timeJump {
  animation: my-face 5s infinite ease-in-out;
  -webkit-animation: my-face 5s infinite ease-in-out;
  display: inline-block;
  margin: 0 5px;
}
@-webkit-keyframes my-face {
  2% {
    -webkit-transform: translate(0, 1.5px) rotate(1.5deg);
    -moz-transform: translate(0, 1.5px) rotate(1.5deg);
    -ms-transform: translate(0, 1.5px) rotate(1.5deg);
    -o-transform: translate(0, 1.5px) rotate(1.5deg);
    transform: translate(0, 1.5px) rotate(1.5deg);
  }
  4% {
    -webkit-transform: translate(0, -1.5px) rotate(-0.5deg);
    -moz-transform: translate(0, -1.5px) rotate(-0.5deg);
    -ms-transform: translate(0, -1.5px) rotate(-0.5deg);
    -o-transform: translate(0, -1.5px) rotate(-0.5deg);
    transform: translate(0, -1.5px) rotate(-0.5deg);
  }
  6% {
    -webkit-transform: translate(0, 1.5px) rotate(-1.5deg);
    -moz-transform: translate(0, 1.5px) rotate(-1.5deg);
    -ms-transform: translate(0, 1.5px) rotate(-1.5deg);
    -o-transform: translate(0, 1.5px) rotate(-1.5deg);
    transform: translate(0, 1.5px) rotate(-1.5deg);
  }
  8% {
    -webkit-transform: translate(0, -1.5px) rotate(-1.5deg);
    -moz-transform: translate(0, -1.5px) rotate(-1.5deg);
    -ms-transform: translate(0, -1.5px) rotate(-1.5deg);
    -o-transform: translate(0, -1.5px) rotate(-1.5deg);
    transform: translate(0, -1.5px) rotate(-1.5deg);
  }
  10% {
    -webkit-transform: translate(0, 2.5px) rotate(1.5deg);
    -moz-transform: translate(0, 2.5px) rotate(1.5deg);
    -ms-transform: translate(0, 2.5px) rotate(1.5deg);
    -o-transform: translate(0, 2.5px) rotate(1.5deg);
    transform: translate(0, 2.5px) rotate(1.5deg);
  }
  12% {
    -webkit-transform: translate(0, -0.5px) rotate(1.5deg);
    -moz-transform: translate(0, -0.5px) rotate(1.5deg);
    -ms-transform: translate(0, -0.5px) rotate(1.5deg);
    -o-transform: translate(0, -0.5px) rotate(1.5deg);
    transform: translate(0, -0.5px) rotate(1.5deg);
  }
  14% {
    -webkit-transform: translate(0, -1.5px) rotate(1.5deg);
    -moz-transform: translate(0, -1.5px) rotate(1.5deg);
    -ms-transform: translate(0, -1.5px) rotate(1.5deg);
    -o-transform: translate(0, -1.5px) rotate(1.5deg);
    transform: translate(0, -1.5px) rotate(1.5deg);
  }
  16% {
    -webkit-transform: translate(0, -0.5px) rotate(-1.5deg);
    -moz-transform: translate(0, -0.5px) rotate(-1.5deg);
    -ms-transform: translate(0, -0.5px) rotate(-1.5deg);
    -o-transform: translate(0, -0.5px) rotate(-1.5deg);
    transform: translate(0, -0.5px) rotate(-1.5deg);
  }
  18% {
    -webkit-transform: translate(0, 0.5px) rotate(-1.5deg);
    -moz-transform: translate(0, 0.5px) rotate(-1.5deg);
    -ms-transform: translate(0, 0.5px) rotate(-1.5deg);
    -o-transform: translate(0, 0.5px) rotate(-1.5deg);
    transform: translate(0, 0.5px) rotate(-1.5deg);
  }
  20% {
    -webkit-transform: translate(0, -1.5px) rotate(2.5deg);
    -moz-transform: translate(0, -1.5px) rotate(2.5deg);
    -ms-transform: translate(0, -1.5px) rotate(2.5deg);
    -o-transform: translate(0, -1.5px) rotate(2.5deg);
    transform: translate(0, -1.5px) rotate(2.5deg);
  }
  22% {
    -webkit-transform: translate(0, 0.5px) rotate(-1.5deg);
    -moz-transform: translate(0, 0.5px) rotate(-1.5deg);
    -ms-transform: translate(0, 0.5px) rotate(-1.5deg);
    -o-transform: translate(0, 0.5px) rotate(-1.5deg);
    transform: translate(0, 0.5px) rotate(-1.5deg);
  }
  24% {
    -webkit-transform: translate(0, 1.5px) rotate(1.5deg);
    -moz-transform: translate(0, 1.5px) rotate(1.5deg);
    -ms-transform: translate(0, 1.5px) rotate(1.5deg);
    -o-transform: translate(0, 1.5px) rotate(1.5deg);
    transform: translate(0, 1.5px) rotate(1.5deg);
  }
  26% {
    -webkit-transform: translate(0, 0.5px) rotate(0.5deg);
    -moz-transform: translate(0, 0.5px) rotate(0.5deg);
    -ms-transform: translate(0, 0.5px) rotate(0.5deg);
    -o-transform: translate(0, 0.5px) rotate(0.5deg);
    transform: translate(0, 0.5px) rotate(0.5deg);
  }
  28% {
    -webkit-transform: translate(0, 0.5px) rotate(1.5deg);
    -moz-transform: translate(0, 0.5px) rotate(1.5deg);
    -ms-transform: translate(0, 0.5px) rotate(1.5deg);
    -o-transform: translate(0, 0.5px) rotate(1.5deg);
    transform: translate(0, 0.5px) rotate(1.5deg);
  }
  30% {
    -webkit-transform: translate(0, -0.5px) rotate(2.5deg);
    -moz-transform: translate(0, -0.5px) rotate(2.5deg);
    -ms-transform: translate(0, -0.5px) rotate(2.5deg);
    -o-transform: translate(0, -0.5px) rotate(2.5deg);
    transform: translate(0, -0.5px) rotate(2.5deg);
  }
  32% {
    -webkit-transform: translate(0, 1.5px) rotate(-0.5deg);
    -moz-transform: translate(0, 1.5px) rotate(-0.5deg);
    -ms-transform: translate(0, 1.5px) rotate(-0.5deg);
    -o-transform: translate(0, 1.5px) rotate(-0.5deg);
    transform: translate(0, 1.5px) rotate(-0.5deg);
  }
  34% {
    -webkit-transform: translate(0, 1.5px) rotate(-0.5deg);
    -moz-transform: translate(0, 1.5px) rotate(-0.5deg);
    -ms-transform: translate(0, 1.5px) rotate(-0.5deg);
    -o-transform: translate(0, 1.5px) rotate(-0.5deg);
    transform: translate(0, 1.5px) rotate(-0.5deg);
  }
  36% {
    -webkit-transform: translate(0, -1.5px) rotate(2.5deg);
    -moz-transform: translate(0, -1.5px) rotate(2.5deg);
    -ms-transform: translate(0, -1.5px) rotate(2.5deg);
    -o-transform: translate(0, -1.5px) rotate(2.5deg);
    transform: translate(0, -1.5px) rotate(2.5deg);
  }
  38% {
    -webkit-transform: translate(0, 1.5px) rotate(-1.5deg);
    -moz-transform: translate(0, 1.5px) rotate(-1.5deg);
    -ms-transform: translate(0, 1.5px) rotate(-1.5deg);
    -o-transform: translate(0, 1.5px) rotate(-1.5deg);
    transform: translate(0, 1.5px) rotate(-1.5deg);
  }
  40% {
    -webkit-transform: translate(0, -0.5px) rotate(2.5deg);
    -moz-transform: translate(0, -0.5px) rotate(2.5deg);
    -ms-transform: translate(0, -0.5px) rotate(2.5deg);
    -o-transform: translate(0, -0.5px) rotate(2.5deg);
    transform: translate(0, -0.5px) rotate(2.5deg);
  }
  42% {
    -webkit-transform: translate(0, 2.5px) rotate(-1.5deg);
    -moz-transform: translate(0, 2.5px) rotate(-1.5deg);
    -ms-transform: translate(0, 2.5px) rotate(-1.5deg);
    -o-transform: translate(0, 2.5px) rotate(-1.5deg);
    transform: translate(0, 2.5px) rotate(-1.5deg);
  }
  44% {
    -webkit-transform: translate(0, 1.5px) rotate(0.5deg);
    -moz-transform: translate(0, 1.5px) rotate(0.5deg);
    -ms-transform: translate(0, 1.5px) rotate(0.5deg);
    -o-transform: translate(0, 1.5px) rotate(0.5deg);
    transform: translate(0, 1.5px) rotate(0.5deg);
  }
  46% {
    -webkit-transform: translate(0, -1.5px) rotate(2.5deg);
    -moz-transform: translate(0, -1.5px) rotate(2.5deg);
    -ms-transform: translate(0, -1.5px) rotate(2.5deg);
    -o-transform: translate(0, -1.5px) rotate(2.5deg);
    transform: translate(0, -1.5px) rotate(2.5deg);
  }
  48% {
    -webkit-transform: translate(0, -0.5px) rotate(0.5deg);
    -moz-transform: translate(0, -0.5px) rotate(0.5deg);
    -ms-transform: translate(0, -0.5px) rotate(0.5deg);
    -o-transform: translate(0, -0.5px) rotate(0.5deg);
    transform: translate(0, -0.5px) rotate(0.5deg);
  }
  50% {
    -webkit-transform: translate(0, 0.5px) rotate(0.5deg);
    -moz-transform: translate(0, 0.5px) rotate(0.5deg);
    -ms-transform: translate(0, 0.5px) rotate(0.5deg);
    -o-transform: translate(0, 0.5px) rotate(0.5deg);
    transform: translate(0, 0.5px) rotate(0.5deg);
  }
  52% {
    -webkit-transform: translate(0, 2.5px) rotate(2.5deg);
    -moz-transform: translate(0, 2.5px) rotate(2.5deg);
    -ms-transform: translate(0, 2.5px) rotate(2.5deg);
    -o-transform: translate(0, 2.5px) rotate(2.5deg);
    transform: translate(0, 2.5px) rotate(2.5deg);
  }
  54% {
    -webkit-transform: translate(0, -1.5px) rotate(1.5deg);
    -moz-transform: translate(0, -1.5px) rotate(1.5deg);
    -ms-transform: translate(0, -1.5px) rotate(1.5deg);
    -o-transform: translate(0, -1.5px) rotate(1.5deg);
    transform: translate(0, -1.5px) rotate(1.5deg);
  }
  56% {
    -webkit-transform: translate(0, 2.5px) rotate(2.5deg);
    -moz-transform: translate(0, 2.5px) rotate(2.5deg);
    -ms-transform: translate(0, 2.5px) rotate(2.5deg);
    -o-transform: translate(0, 2.5px) rotate(2.5deg);
    transform: translate(0, 2.5px) rotate(2.5deg);
  }
  58% {
    -webkit-transform: translate(0, 0.5px) rotate(2.5deg);
    -moz-transform: translate(0, 0.5px) rotate(2.5deg);
    -ms-transform: translate(0, 0.5px) rotate(2.5deg);
    -o-transform: translate(0, 0.5px) rotate(2.5deg);
    transform: translate(0, 0.5px) rotate(2.5deg);
  }
  60% {
    -webkit-transform: translate(0, 2.5px) rotate(2.5deg);
    -moz-transform: translate(0, 2.5px) rotate(2.5deg);
    -ms-transform: translate(0, 2.5px) rotate(2.5deg);
    -o-transform: translate(0, 2.5px) rotate(2.5deg);
    transform: translate(0, 2.5px) rotate(2.5deg);
  }
  62% {
    -webkit-transform: translate(0, -0.5px) rotate(2.5deg);
    -moz-transform: translate(0, -0.5px) rotate(2.5deg);
    -ms-transform: translate(0, -0.5px) rotate(2.5deg);
    -o-transform: translate(0, -0.5px) rotate(2.5deg);
    transform: translate(0, -0.5px) rotate(2.5deg);
  }
  64% {
    -webkit-transform: translate(0, -0.5px) rotate(1.5deg);
    -moz-transform: translate(0, -0.5px) rotate(1.5deg);
    -ms-transform: translate(0, -0.5px) rotate(1.5deg);
    -o-transform: translate(0, -0.5px) rotate(1.5deg);
    transform: translate(0, -0.5px) rotate(1.5deg);
  }
  66% {
    -webkit-transform: translate(0, 1.5px) rotate(-0.5deg);
    -moz-transform: translate(0, 1.5px) rotate(-0.5deg);
    -ms-transform: translate(0, 1.5px) rotate(-0.5deg);
    -o-transform: translate(0, 1.5px) rotate(-0.5deg);
    transform: translate(0, 1.5px) rotate(-0.5deg);
  }
  68% {
    -webkit-transform: translate(0, -1.5px) rotate(-0.5deg);
    -moz-transform: translate(0, -1.5px) rotate(-0.5deg);
    -ms-transform: translate(0, -1.5px) rotate(-0.5deg);
    -o-transform: translate(0, -1.5px) rotate(-0.5deg);
    transform: translate(0, -1.5px) rotate(-0.5deg);
  }
  70% {
    -webkit-transform: translate(0, 1.5px) rotate(0.5deg);
    -moz-transform: translate(0, 1.5px) rotate(0.5deg);
    -ms-transform: translate(0, 1.5px) rotate(0.5deg);
    -o-transform: translate(0, 1.5px) rotate(0.5deg);
    transform: translate(0, 1.5px) rotate(0.5deg);
  }
  72% {
    -webkit-transform: translate(0, 2.5px) rotate(1.5deg);
    -moz-transform: translate(0, 2.5px) rotate(1.5deg);
    -ms-transform: translate(0, 2.5px) rotate(1.5deg);
    -o-transform: translate(0, 2.5px) rotate(1.5deg);
    transform: translate(0, 2.5px) rotate(1.5deg);
  }
  74% {
    -webkit-transform: translate(0, -0.5px) rotate(0.5deg);
    -moz-transform: translate(0, -0.5px) rotate(0.5deg);
    -ms-transform: translate(0, -0.5px) rotate(0.5deg);
    -o-transform: translate(0, -0.5px) rotate(0.5deg);
    transform: translate(0, -0.5px) rotate(0.5deg);
  }
  76% {
    -webkit-transform: translate(0, -0.5px) rotate(2.5deg);
    -moz-transform: translate(0, -0.5px) rotate(2.5deg);
    -ms-transform: translate(0, -0.5px) rotate(2.5deg);
    -o-transform: translate(0, -0.5px) rotate(2.5deg);
    transform: translate(0, -0.5px) rotate(2.5deg);
  }
  78% {
    -webkit-transform: translate(0, -0.5px) rotate(1.5deg);
    -moz-transform: translate(0, -0.5px) rotate(1.5deg);
    -ms-transform: translate(0, -0.5px) rotate(1.5deg);
    -o-transform: translate(0, -0.5px) rotate(1.5deg);
    transform: translate(0, -0.5px) rotate(1.5deg);
  }
  80% {
    -webkit-transform: translate(0, 1.5px) rotate(1.5deg);
    -moz-transform: translate(0, 1.5px) rotate(1.5deg);
    -ms-transform: translate(0, 1.5px) rotate(1.5deg);
    -o-transform: translate(0, 1.5px) rotate(1.5deg);
    transform: translate(0, 1.5px) rotate(1.5deg);
  }
  82% {
    -webkit-transform: translate(0, -0.5px) rotate(0.5deg);
    -moz-transform: translate(0, -0.5px) rotate(0.5deg);
    -ms-transform: translate(0, -0.5px) rotate(0.5deg);
    -o-transform: translate(0, -0.5px) rotate(0.5deg);
    transform: translate(0, -0.5px) rotate(0.5deg);
  }
  84% {
    -webkit-transform: translate(0, 1.5px) rotate(2.5deg);
    -moz-transform: translate(0, 1.5px) rotate(2.5deg);
    -ms-transform: translate(0, 1.5px) rotate(2.5deg);
    -o-transform: translate(0, 1.5px) rotate(2.5deg);
    transform: translate(0, 1.5px) rotate(2.5deg);
  }
  86% {
    -webkit-transform: translate(0, -1.5px) rotate(-1.5deg);
    -moz-transform: translate(0, -1.5px) rotate(-1.5deg);
    -ms-transform: translate(0, -1.5px) rotate(-1.5deg);
    -o-transform: translate(0, -1.5px) rotate(-1.5deg);
    transform: translate(0, -1.5px) rotate(-1.5deg);
  }
  88% {
    -webkit-transform: translate(0, -0.5px) rotate(2.5deg);
    -moz-transform: translate(0, -0.5px) rotate(2.5deg);
    -ms-transform: translate(0, -0.5px) rotate(2.5deg);
    -o-transform: translate(0, -0.5px) rotate(2.5deg);
    transform: translate(0, -0.5px) rotate(2.5deg);
  }
  90% {
    -webkit-transform: translate(0, 2.5px) rotate(-0.5deg);
    -moz-transform: translate(0, 2.5px) rotate(-0.5deg);
    -ms-transform: translate(0, 2.5px) rotate(-0.5deg);
    -o-transform: translate(0, 2.5px) rotate(-0.5deg);
    transform: translate(0, 2.5px) rotate(-0.5deg);
  }
  92% {
    -webkit-transform: translate(0, 0.5px) rotate(-0.5deg);
    -moz-transform: translate(0, 0.5px) rotate(-0.5deg);
    -ms-transform: translate(0, 0.5px) rotate(-0.5deg);
    -o-transform: translate(0, 0.5px) rotate(-0.5deg);
    transform: translate(0, 0.5px) rotate(-0.5deg);
  }
  94% {
    -webkit-transform: translate(0, 2.5px) rotate(0.5deg);
    -moz-transform: translate(0, 2.5px) rotate(0.5deg);
    -ms-transform: translate(0, 2.5px) rotate(0.5deg);
    -o-transform: translate(0, 2.5px) rotate(0.5deg);
    transform: translate(0, 2.5px) rotate(0.5deg);
  }
  96% {
    -webkit-transform: translate(0, -0.5px) rotate(1.5deg);
    -moz-transform: translate(0, -0.5px) rotate(1.5deg);
    -ms-transform: translate(0, -0.5px) rotate(1.5deg);
    -o-transform: translate(0, -0.5px) rotate(1.5deg);
    transform: translate(0, -0.5px) rotate(1.5deg);
  }
  98% {
    -webkit-transform: translate(0, -1.5px) rotate(-0.5deg);
    -moz-transform: translate(0, -1.5px) rotate(-0.5deg);
    -ms-transform: translate(0, -1.5px) rotate(-0.5deg);
    -o-transform: translate(0, -1.5px) rotate(-0.5deg);
    transform: translate(0, -1.5px) rotate(-0.5deg);
  }
  0%,
  100% {
    -webkit-transform: translate(0, 0) rotate(0);
    -moz-transform: translate(0, 0) rotate(0);
    -ms-transform: translate(0, 0) rotate(0);
    -o-transform: translate(0, 0) rotate(0);
    transform: translate(0, 0) rotate(0);
  }
}
</style>
