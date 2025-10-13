<template>
    <CardBase :title="$t('V3C18L0')" :content="$t('V3C18L1')" :card-number="18" :background-front-image="`C18.${imageType}`">
        <template v-slot:back-content>
            <div id="card18-back-label1" class="label set-one">
                <p id="card18-back-text1">{{ $t('V3C0L0') + ' ' + "1"}}</p>
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