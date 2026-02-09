<template>
    <CardBase :title="$t('V3C8L0')" :content="$t('V3C8L1')" :card-number="8" :background-front-image="`C8.${imageType}`">
        <template v-slot:back-content>
            <div class="label black number">
                <p>12</p>
            </div> 
            <div id="card8-back-label1" class="label set-one">
                <p id="card8-back-text1">{{ $t('V3C0L0') + ' ' + "2"}}</p>
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