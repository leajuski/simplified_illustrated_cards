<template>
    <CardBase :title="$t('V1C39L1')" :content="$t('V1C39L2')" :card-number="39" :background-front-image="`C39.${imageType}`">
        <template v-slot:back-content>
            <div id="card39-back-label1" class="label set-one">
                <p id="card39-back-text1">{{ $t('V3C0L0') + ' ' + "5"}}</p>
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