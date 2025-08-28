<template>
    <CardBase :title="$t('V3C26L0')" :content="$t('V3C26L1')" :card-number="26" :background-front-image="`C26.${imageType}`">
        <template v-slot:back-content>
            <div id="card26-back-label1" class="label set-one">
                <p id="card26-back-text1">{{ $t('V3C0L0') + ' ' + "4"}}</p>
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