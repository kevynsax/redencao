<template>
    <div class="social-network" @click="openLink">
        <img :src="image" :alt="symbol"/>
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

    public get image(): string {
        return require(`../../assets/${this.symbol.toLowerCase()}.png`);
    }
}

</script>

<style scoped lang="scss">
.social-network {
    border-radius: 4px;

    color: #ffffff;

    cursor: pointer;

    &:hover{
        img{
            filter: invert(.3);
        }
    }
}
</style>
