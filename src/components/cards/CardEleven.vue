<template>
    <CardBase :title="$t('V3C11L0')" :content="$t('V3C11L1')" :card-number="11" :background-front-image="`C11.${imageType}`" >
        <template v-slot:back-content>
            <div id="card11-back-label2" class="label set-one">
                <p id="card11-back-text2">{{ $t('V3C0L0') + ' ' + "2"}}</p>
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