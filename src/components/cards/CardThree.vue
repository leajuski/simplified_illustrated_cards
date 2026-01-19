<template>
    <CardBase :title="$t('V3C3L0')" :content="$t('V3C3L1')" :card-number="3"
        :background-front-image="`C3.${imageType}`" >
        <template v-slot:back-content>
            <div id="card3-back-label1" class="label black set-one">
                <p id="card3-back-text1">{{ $t('V3C0L0') + ' ' + "2"}}</p>
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