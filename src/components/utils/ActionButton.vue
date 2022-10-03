<template>
  <div class="action-button" @click="onAction">
    <span>{{ action }}</span>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

@Options({
  props: {
    action: String,
    link: String,
  },
})
export default class ActionButton extends Vue {
  action!: string;
  link!: string;

  private onAction(): void {
    window.open(this.link, '_blank');
  };
}
</script>

<style scoped lang="scss">
.action-button {
  padding: 8px 16px;
  border-radius: 4px;

  background-color: rgb(253, 218, 13);

  cursor: pointer;
}
</style>
