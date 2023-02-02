<template>
    <div class="banner" :style="{'background-color': background}">
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
        background: {
            type: String,
            default: 'whitesmoke'
        },
        action: ActionButton,
    },
})
export default class Banner extends Vue {
    title!: string;
    subtitle!: string;
    warn!: string;
    background!: string;
    action!: ActionButton;
}
</script>

<style scoped lang="scss">
.banner {
    padding: 32px;

    span {
        display: block;
        text-align: center;
        margin-top: 8px;

        &:first-child {
            margin-top: unset;
            font-weight: bold;
            font-size: 22px;
        }
    }

    .warn {
        color: darkred;
        font-weight: bold;
    }
}
</style>
