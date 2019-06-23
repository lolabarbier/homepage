<template>
  <div id="container">
    <Marquee/>
    <AboutMe/>
    <PrizeButton/>
  </div>
</template>

<script>
import Marquee from './components/Marquee.vue';
import AboutMe from './components/AboutMe.vue';
import PrizeButton from './components/PrizeButton.vue';


export default {
  name: 'Homepage',
  components: { Marquee, AboutMe, PrizeButton }
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
</style>
