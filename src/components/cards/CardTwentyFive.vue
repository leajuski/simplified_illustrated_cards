<template>
    <CardBase :title="$t('V3C25L0')" :content="$t('V3C25L1')" :card-number="25" :background-front-image="`C25.${imageType}`">
        <template v-slot:back-content>
            <div class="label black number">
                <p>25</p>
            </div> 
            <div id="card25-back-label1" class="label set-one">
                <p id="card25-back-text1">{{ $t('V3C0L0') + ' ' + "4"}}</p>
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