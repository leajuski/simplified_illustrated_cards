<template>
    <CardBase :title="$t('V3C13L0')" :content="$t('V3C13L1')" :card-number="13" :background-front-image="`C13.${imageType}`">
        <template v-slot:back-content>
            <div id="card13-back-label1" class="label set-one">
                <p id="card13-back-text1">{{ $t('V3C0L0') + ' ' + "1"}}</p>
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

<!-- pour une résolution de 470x693 -->
<style>
.card13-label1-position {
    top: calc(141px * var(--scale-factor));
    left: calc(142.7px * var(--scale-factor));
    width: calc(113.5px * var(--scale-factor));
    height: calc(37.8px * var(--scale-factor));
    font-size: calc(14px * var(--scale-factor));
    /* border : solid red 0.5px * var(--scale-factor)); */
}

.card13-label2-position {
    top: calc(215.8px * var(--scale-factor));
    left: calc(30px * var(--scale-factor));
    width: calc(87.7px * var(--scale-factor));
    height: calc(37.8px * var(--scale-factor));
    font-size: calc(14px * var(--scale-factor));
    /* border : solid red 0.5px * var(--scale-factor)); */
}

.card13-label3-position {
    top: calc(101.5px * var(--scale-factor));
    left: calc(370px * var(--scale-factor));
    width: calc(146px * var(--scale-factor));
    height: calc(37.8px * var(--scale-factor));
    font-size: calc(14px * var(--scale-factor));
    /* border : solid red 0.5px * var(--scale-factor)); */
}

.card13-label4-position {
    top: calc(215.8px * var(--scale-factor));
    left: calc(430px * var(--scale-factor));
    width: calc(86px * var(--scale-factor));
    height: calc(37.8px * var(--scale-factor));
    font-size: calc(14px * var(--scale-factor));
    /* border : solid red 0.5px * var(--scale-factor)); */
}

.card13-label5-position {
    top: calc(157.4px * var(--scale-factor));
    left: calc(473px * var(--scale-factor));
    width: calc(57.6px * var(--scale-factor));
    height: calc(18.9px * var(--scale-factor));
    font-size: calc(17px * var(--scale-factor));
    color: white;
}

.card13-label6-position {
    top: calc(289.9px * var(--scale-factor));
    left: calc(473px * var(--scale-factor));
    width: calc(57.6px * var(--scale-factor));
    height: calc(18.9px * var(--scale-factor));
    font-size: calc(17px * var(--scale-factor));
    color: white;
}

.card13-fixed-label3-position {
    top: calc(341px * var(--scale-factor));
    left: calc(513.4px * var(--scale-factor));
    width: calc(57.6px * var(--scale-factor));
    height: calc(18.9px * var(--scale-factor));
    font-size: calc(20.7px * var(--scale-factor));
    color: white;
}
</style>
