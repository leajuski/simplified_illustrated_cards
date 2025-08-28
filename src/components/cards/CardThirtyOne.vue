<template>
    <CardBase :title="$t('V1C31L1')" :content="$t('V1C31L2')" :card-number="31" :background-front-image="`C31.${imageType}`" >
        <template v-slot:back-content>
            <div id="card31-back-label1" class="label set-one">
                <p id="card31-back-text1">{{ $t('V3C0L0') + ' ' + "5"}}</p>
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