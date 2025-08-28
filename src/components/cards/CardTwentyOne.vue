<template>
    <CardBase :title="$t('V3C21L0')" :content="$t('V3C21L0')" :card-number="21" :background-front-image="`C21.${imageType}`"> 
        <div id="card21-label1" class="horizontal-center label black card21-label1-position">
            <p id="card21-text1" class="font-medium">{{ $t('V1C21L6') }}</p>
        </div>
        <template v-slot:back-content>
            <div id="card21-back-label2" class="label set-one">
                <p id="card21-back-text2">{{ $t('V3C0L0') + ' ' + "1"}}</p>
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