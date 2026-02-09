<template>
    <CardBase :title="$t('V3C19L0')" :content="$t('V3C19L1')" :card-number="19" :background-front-image="`C19.${imageType}`">
        <template v-slot:back-content>
            <div class="label black number">
                <p>16</p>
            </div> 
            <div id="card19-back-label1" class="label set-one">
                <p id="card19-back-text1">{{ $t('V3C0L0') + ' ' + "3"}}</p>
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