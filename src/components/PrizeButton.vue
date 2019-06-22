<template>
  <button id="prize-button"
    v-bind:style="{ top: top + '%', left: left + '%' }"
    @mouseover="handleMouseOver">
    <p>click 2 win fabuluos prize !!!</p>
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
    }
  },
  methods: {
    handleMouseOver() {
      this.top = Math.floor(Math.random() * Math.floor(100));
      this.left = Math.floor(Math.random() * Math.floor(80));
      // handle laughter
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
