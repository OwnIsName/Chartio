<template>
  <div class='header'>
    <div class="logo">
      <div class="box">c.io</div>
      <div class="text">
        <span class="first">chart</span>
        <span class="second">.io</span>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Header',
  data () {
    return {
    }
  }
}
</script>
<style lang="scss" scoped>

.header {
  width: 100%;
  height: 80px;
  background-color: #3f51b5;
  font-family: 'Lato', sans-serif;
}

.logo {
  height: 60px;
  position: relative;
  left: 50%;
  display: inline-block;
  transform: translate(-50%);
  margin: 0 auto;
  padding: 10px 0;
}

.box {
  width: 60px;
  height: 60px;
  border: 1px solid rgba(0, 0, 0, .5);
  border-radius: 10px;
  background: #ff5722;
  color: #fff;
  font-size: 26px;
  font-weight: 700;
  line-height: 60px;
  text-align: center;
  font-style: italic;
  position: absolute;
  left: 0%;
  z-index: 2;
  animation: animate 2s;
}

.box:after {
  content: "";
  display: block;
  height: 90%;
  width: 1px;
  background: #fff;
  position: absolute;
  top: 0;
  right: -10px;
  bottom: 0;
  margin: auto;
  animation: expand 2s;
}

.text {
  height: 60px;
  color: #fff;
  padding-left: 80px;
  line-height: 60px;
  font-size: 30px;
  font-weight: 300;
  animation: fade 2.5s;
}

@keyframes expand {
  0% {
    height: 0;
  }
  40% {
    height: 0;
  }
  60% {
    height: 80%;
  }
}

@keyframes animate {
  0% {
    transform: scale(0);
    left: 39%;
  }
  40% {
    transform: scale(1);
    left: 39%;
  }
  60% {
    transform: scale(1);
    left: 39%;
  }
  100% {
    left: 0%;
  }
}

@keyframes fade {
  0% {
    opacity: 0;
  }
  65% {
    opacity: 0;
    padding-left: 70px;
  }
  100% {
    opacity: 1;
    padding-left: 80px;
  }
}

</style>
