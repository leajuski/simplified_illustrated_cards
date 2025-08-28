<template>
    <CardBase :title="$t('V3C40L0')" :content="$t('V3C40L1')" :card-number="40" :background-front-image="`C40.${imageType}`">
        <template v-slot:back-content>
            <div id="card40-back-label1" class="label set-one">
                <p id="card40-back-text1">{{ $t('V3C0L0') + ' ' + "5"}}</p>
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