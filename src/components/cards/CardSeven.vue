<template>
    <CardBase :title="$t('V3C7L0')" :content="$t('V3C7L1')" :card-number="7" :background-front-image="`C7.${imageType}`">
        <template v-slot:back-content>
            <div id="card7-back-label1" class="label set-one">
                <p id="card7-back-text1">{{ $t('V3C0L0') + ' ' + "2"}}</p>
            </div>
        </template>
    </CardBase>
</template>

<script>
import CardBase from "@/components/base/CardBase.vue";

export default {
    name: "CardOne",
    components: {
        CardBase,
    },
    data() {
        return {
            imageType: process.env.VUE_APP_IMAGE_TYPE || 'png',
        };
    },
};
</script>

<!-- pour une résolution de 470x693 -->
<style>
.card7-label1-position {
    top: 24.6vh;
    left: 12.7vw;
    width: 74.8vw;
    height: 6.88vh;
    /* border: solid red; */
}

.card7-label2-position {
    top: calc(261.4px * var(--scale-factor));
    left: calc(216.7px * var(--scale-factor));
    width: calc(168px * var(--scale-factor));
    height: calc(31.8px * var(--scale-factor));
    text-align: left;
    font-size: calc(17px * var(--scale-factor));
    /* border: solid red; */
}

.card7-label3-position {
    top: calc(325px * var(--scale-factor));
    left: calc(215.8px * var(--scale-factor));
    width: calc(127.3px * var(--scale-factor));
    height: calc(31.8px * var(--scale-factor));
    text-align: left;
    font-size: calc(17px * var(--scale-factor));
    /* border: solid red; */
}
</style>