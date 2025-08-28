<template>
    <CardBase :title="$t('V3C38L0')" :content="$t('V3C38L0')" :card-number="38" :background-front-image="`C38.${imageType}`">
        <template v-slot:back-content>
            <div id="card38-back-label1" class="label set-one">
                <p id="card38-back-text1">{{ $t('V3C0L0') + ' ' + "5"}}</p>
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