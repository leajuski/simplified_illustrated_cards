<template>
    <CardBase :title="$t('V3C22L0')" :content="$t('V3C22L1')" :card-number="22" :background-front-image="`C22.${imageType}`">
        <template v-slot:back-content>
            <div class="label black number">
                <p>24</p>
            </div> 
            <div id="card22-back-label1" class="label set-one">
                <p id="card22-back-text1">{{ $t('V3C0L0') + ' ' + "4"}}</p>
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