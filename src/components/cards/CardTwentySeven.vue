<template>
    <CardBase :title="$t('V3C27L0')" :content="$t('V3C27L1')" :card-number="27" :background-front-image="`C27.${imageType}`">
        <template v-slot:back-content>
            <div id="card27-back-label1" class="label set-one">
                <p id="card27-back-text1">{{ $t('V3C0L0') + ' ' + "4"}}</p>
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