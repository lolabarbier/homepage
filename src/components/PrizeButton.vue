<template>
  <button id="prize-button"
    v-bind:style="{ top: top + '%', left: left + '%' }"
    @mouseover="handleMouseOver"
    @click="handleClick"
  >
    <p>click 2 win fabolous prize !!!</p>
    <audio id="laugh1" :src="audio.laugh1" hidden></audio>
    <audio id="laugh2" :src="audio.laugh2" hidden></audio>
    <audio id="laugh3" :src="audio.laugh3" hidden></audio>
    <audio id="laugh4" :src="audio.laugh4" hidden></audio>
  </button>
</template>

<script>

export default {
  name: 'PrizeButton',
  components: {},
  data: function (){
    return {
      top: 60,
      left: 10,
      audio: {
        laugh1: require('../assets/laugh1.mp3'),
        laugh2: require('../assets/laugh2.mp3'),
        laugh3: require('../assets/laugh3.mp3'),
        laugh4: require('../assets/laugh4.mp3'),
      }
    }
  },
  methods: {
    handleMouseOver() {
      this.mockCruelly();
      this.top = Math.floor(Math.random() * Math.floor(100));
      this.left = Math.floor(Math.random() * Math.floor(80));
    },
    mockCruelly() {
      const laughs = Object.keys(this.audio);
      const laugh = laughs[laughs.length * Math.random() << 0];

      document.getElementById(`${laugh}`).play();
    },
    handleClick() {
      window.alert('you got him but u cheated >:(');
    }
  }
}
</script>

<style lang="scss">
#prize-button {
  position: absolute;
  z-index: 2000;
  padding: 10px 15px;
  background: yellow;
  border-top: 5px solid #ccc;
  border-left: 5px solid #ccc;
  border-bottom: 5px solid #999;
  border-right: 5px solid #999;

  p {
    animation: blinker .1s linear infinite;
    margin: 0;
    color: magenta;
    font-weight: bold;
  }

  @keyframes blinker {
    50% {
      opacity: 0;
    }
  }
}
</style>
