<template>
  <div id="christmas">
    <div class='luckor' v-for='dag in dagar' >
      <Lucka :dag='dag' />
    </div>
  </div>
</template>

<script>
  import Lucka from './Lucka.vue';

  export default {
    name: 'Background',
    components: {
      Lucka
    },
    computed: {
      dagar() {
        return this.$store.state.dagar
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  #christmas {
    display: flex;
    flex-wrap: wrap;
  }
  .luckor {
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
