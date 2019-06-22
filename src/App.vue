<template>
  <div id="container">
    <Marquee/>
    <div id="about-me">
      <b>hi i'm <u>l o l a</u></b>
      <br>
      <br>
      i like many things but i make my living as a web developer
      <br>
      <br>
      i live in paris and am not super sure what to put in this space yet
    </div>
    <PrizeButton/>
  </div>
</template>

<script>
import Marquee from './components/Marquee.vue'
import PrizeButton from './components/PrizeButton.vue'


export default {
  name: 'Homepage',
  components: { Marquee, PrizeButton }
}
</script>

<style lang="scss">
body {
  background: url('./assets/gegebg.png') repeat;
  background-size: 350px;
}

#container {
  width: 100%;
  height: 95vh;
  display: flex;
  flex-direction: column;
  align-items: center;
}

#about-me {
  background: white;
  opacity: .6;
  width: 200px;
  font-family: monospace, monospace;
  font-size: 12px;
  border: 5px dashed orange;
  outline: 5px dotted blue;
  padding: 20px;
}
</style>
