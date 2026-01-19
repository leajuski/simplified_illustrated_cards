<template>
    <CardBase :title="$t('V3C21L0')" :content="$t('V3C21L1')" :card-number="21" :background-front-image="`C21.${imageType}`"> 
        <template v-slot:back-content>
            <div id="card21-back-label1" class="label set-one">
                <p id="card21-back-text1">{{ $t('V3C0L0') + ' ' + "3"}}</p>
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