<template>
    <CardBase :title="$t('V3C1L0')" :content="$t('V3C1L1')" :card-number="1" :background-front-image="`C1.${imageType}`">
        <template v-slot:back-content>
            <div id="card1-back-label1" class="label black set-one">
                <p id="card1-back-text1">{{ $t('V3C0L0') + ' ' + "1"}}</p>
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

<style>

#card1-text0 {
    color : white;
}

</style>