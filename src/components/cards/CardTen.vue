<template>
    <CardBase :title="$t('V3C10L0')" :content="$t('V3C10L1')" :card-number="10" :background-front-image="`C10.${imageType}`">
        <template v-slot:back-content>
            <div id="card10-back-label1" class="label set-one">
                <p id="card10-back-text1">{{ $t('V3C0L0') + ' ' + "3"}}</p>
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