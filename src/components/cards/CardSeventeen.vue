<template>
    <CardBase :title="$t('V3C17L0')" :content="$t('V3C17L1')" :card-number="17" :background-front-image="`C17.${imageType}`" >
        <template v-slot:back-content>
            <div class="label black number">
                <p>15</p>
            </div> 
            <div id="card17-back-label1" class="label set-one">
                <p id="card17-back-text1">{{ $t('V3C0L0') + ' ' + "3"}}</p>
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