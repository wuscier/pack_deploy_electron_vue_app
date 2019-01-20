<template>
  <div>

    <div>
      <span>url("../../../static/img/ku.png")</span>
      <div class="img-background1">img background</div>
    </div>

    <hr>

    <div>
      <span>url("/static/img/ku.png")</span>
      <div class="img-background2">img background</div>
    </div>

    <hr>

    <div>
      <span>../../../static/img/ku.png</span>
      <img src="../../../static/img/ku.png">
    </div>
    
    <hr>
    <div>
      <span>/static/img/ku.png</span>
      <img src="/static/img/ku.png">
    </div>

    <hr>

    <div v-for="(hardware, index) in hardwares1" :key="index">
      <span>{{hardware.icon}}</span>
      <img :src="hardware.icon">
    </div>

    <hr>
    <div>
      <div v-for="(hardware, index) in hardwares2" :key="index">
        <span>{{hardware.icon}}</span>
        <img :src="hardware.icon">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      hardwares1: [
        { icon: require("../../../static/img/ku.png") },
        { icon: require("../../../static/img/result.png") }
      ],
      hardwares2: [
        { icon: require("../../../static/img/ku.png") },
        { icon: require("../../../static/img/result.png") }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
img {
  width: 50px;
  height: 50px;
}
.img-background1 {
  width: 50px;
  height: 50px;
  background-size: 50px, 50px;
  background-image: url("../../../static/img/ku.png");
}
.img-background2 {
  width: 50px;
  height: 50px;
  background-size: 50px, 50px;
  background-image: url("/static/img/ku.png");
}
</style>
