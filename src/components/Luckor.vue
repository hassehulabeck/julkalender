<template>
  <section>
    <div v-for='dag in dagar' :key='dag.datum'
    @click='toggle()'>
      <h1 v-show="!showIt"> {{ dag.datum }} </h1>
      <p v-show="showIt"> {{ dag.lottNummer }} </p>
    </div>
  </section>
</template>

<script>



export default {
  name: 'Luckor',
  data: function() {
    return {
      showIt: false
    }
  },
  computed: {
    dagar() {
      return this.$store.state.dagar
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
  div {
    border: 2px dotted white;
    border-left: none;
    box-shadow: 1px 1px 14px silver;
    width: 3em;
    height: 3em;
    flex: 0 1 auto;
    margin: 1em;
    padding: 1em;
    flex: 0 1 auto;
    display: inline-flex;
  }
</style>
