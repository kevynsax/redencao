<template>
  <Homepage />
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Homepage from './components/Homepage.vue';

@Options({
  components: {
    Homepage,
  },
})
export default class App extends Vue {}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
