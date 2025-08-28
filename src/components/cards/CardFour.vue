<template>
    <CardBase :title="$t('V3C4L0')" :content="$t('V3C4L1')" :card-number="4"
        :background-front-image="`C4.${imageType}`">
        <template v-slot:back-content>
            <div id="card4-back-label1" class="label set-one">
                <p id="card4-back-text1">{{ $t('V3C0L0') + ' ' + "2"}}</p>
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