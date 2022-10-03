<template>
  <div class="social-network" @click="openLink">
    <span>{{ symbol }}</span>
    <slot></slot>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

@Options({
  props: {
    symbol: String,
    link: String,
  },
})
export default class SocialNetwork extends Vue {
  symbol!: string;
  link!: string;

  private openLink(): void {
    window.open(this.link, '_blank');
  };
}

</script>

<style scoped lang="scss">
.social-network {
  padding: 8px 16px;
  border-radius: 4px;

  background-color: #000000;
  color: #ffffff;

  cursor: pointer;
}
</style>
