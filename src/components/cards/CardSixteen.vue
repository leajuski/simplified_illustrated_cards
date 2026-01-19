<template>
    <CardBase :title="$t('V3C16L0')" :content="$t('V3C16L1')" :card-number="16" :background-front-image="`C16.${imageType}`">
        <template v-slot:back-content>
            <div id="card16-back-label1" class="label set-one">
                <p id="card16-back-text1">{{ $t('V3C0L0') + ' ' + "2"}}</p>
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