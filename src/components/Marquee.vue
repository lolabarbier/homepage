<template>
  <div id="marquee-container">
    <div id="marquee">
      <p class="sparkles">*✲ﾟ*｡⋆</p>
      grahic design is my passion
      <p class="sparkles">⋆｡*ﾟ✲*</p>
      <audio id="audio" src="../assets/gegebg.png"></audio>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Marquee',
  components: {},
  methods: {
  
  }
}
</script>

<style lang="scss">
#marquee-container {
  font-family: "Comic Sans MS", cursive, sans-serif;
  align-self: flex-start;
  width: 100%;
  font-size: 45px;
  overflow: hidden;
  white-space: nowrap;
  color: white;
  margin: 150px 0 30px;
}

#marquee {
  display: flex;
  animation-duration: 2.5s;
  animation-timing-function: linear;
  animation-name: slidein;
  animation-iteration-count: infinite;
  animation-direction: alternate;

  .sparkles {
    background: -webkit-linear-gradient(red, orange, yellow, green, cyan, blue, violet);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    margin: 0 10px;
  }
}

@keyframes slidein {
  from {
    margin-left: -100px;
  }

  to {
    margin-left: 60%;
  }
}
</style>
