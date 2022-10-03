<template>
  <div class="banner">
    <span>{{ title }}</span>
    <span>{{ subtitle }}</span>
    <span class="warn">{{ warn }}</span>
    <slot></slot>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import ActionButton from '@/components/utils/ActionButton.vue';

@Options({
  props: {
    title: String,
    subtitle: String,
    warn: {
      type: String,
      default: '',
    },
    action: ActionButton,
  },
})
export default class Banner extends Vue {
  title!: string;
  subtitle!: string;
  warn!: string;
  action!: ActionButton;
}
</script>

<style scoped lang="scss">
.banner {
  padding: 16px 32px;

  background-color: whitesmoke;

  span {
    display: block;
    text-align: center;
    margin-top: 8px;

    &:first-child {
      margin-top: unset;
      font-weight: bold;
    }
  }

  .warn {
    color: darkred;
  }
}
</style>
