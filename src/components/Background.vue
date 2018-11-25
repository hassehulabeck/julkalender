<template>
  <div id="christmas">
    <Luckor/>
  </div>
</template>

<script>

import Luckor from './Luckor.vue';

export default {
  name: 'Background',
  components: {
    Luckor
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  #christmas {
    display: flex;
  }
</style>
