<template>
  <section @click='toggle'>
      <h1 v-show="!showIt"> {{ dag.datum }} </h1>
      <p v-show="showIt"> {{ dag.lottNummer }} </p>
  </section>
</template>

<script>



export default {
  name: 'Lucka',
  props: ['dag'],
  data: function() {
    return {
      showIt: false
    }
  },
  methods: {
    toggle() {
      this.showIt = !this.showIt;
    }
  }
}
</script>

<style scoped>
  h1 {
    color: yellow;
  }
</style>
