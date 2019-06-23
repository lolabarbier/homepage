<template>
  <div id="about-me">
    <b>hi i'm <u>lola</u></b>
    <br>
    <br>
    i like many things but i make my living as a web developer
    <br>
    <br>
    i live in paris and am not super sure what to put in this space yet
  </div>
</template>

<script>
import _ from 'lodash'; 

export default {
  name: 'AboutMe',
  components: {},
}
</script>

<style lang="scss">
#about-me {
  background: white;
  opacity: .9;
  width: 200px;
  font-family: monospace, monospace;
  font-size: 12px;
  border: 5px dashed #f4932e;
  outline: 5px dotted #461ef9;
  padding: 20px;
}
</style>
