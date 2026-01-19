<template>
    <CardBase :title="$t('V3C14L0')" :content="$t('V3C14L1')" :card-number="14" :background-front-image="`C14.${imageType}`" >
        <template v-slot:back-content>
            <div id="card14-back-label1" class="label set-one">
                <p id="card14-back-text1">{{ $t('V3C0L0') + ' ' + "1"}}</p>
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