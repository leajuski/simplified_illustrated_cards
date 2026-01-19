<template>
    <CardBase :title="$t('V3C20L0')" :content="$t('V3C20L1')" :card-number="20" :background-front-image="`C20.${imageType}`">
        <template v-slot:back-content>
            <div id="card20-back-label1" class="label set-one">
                <p id="card20-back-text1">{{ $t('V3C0L0') + ' ' + "4"}}</p>
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