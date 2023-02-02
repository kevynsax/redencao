<template>
    <div class="action-button" @click="onAction" :style="{'background-color': background}">
        <span>{{ action }}</span>
    </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

@Options({
    props: {
        action: String,
        link: String,
        background: {
            type: String,
            default: 'rgb(253, 218, 13)'
        }
    },
})
export default class ActionButton extends Vue {
    action!: string;
    link!: string;
    background!: string;

    private onAction(): void {
        window.open(this.link, '_blank');
    };
}
</script>

<style scoped lang="scss">
.action-button {
    padding: 8px 24px;
    border-radius: 4px;

    cursor: pointer;
    font-weight: bold;
    &:hover{
        opacity: .7;
    }

}
</style>
