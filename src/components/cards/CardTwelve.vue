<template>
    <CardBase :title="$t('V3C12L0')" :content="$t('V3C12L1')" :card-number="12" :background-front-image="`C12.${imageType}`">
        <div id="card12-label1" class="horizontal-center label black card12-label1-position">
            <p id="card12-text1" class="font-small">{{ $t('V3C12L2') }}</p>
        </div>
        <div id="card12-label2" class="horizontal-center label black card12-label2-position">
            <p id="card12-text2" class="font-small">{{ $t('V3C12L3') }}</p>
        </div>
        <div id="card12-label3" class="horizontal-center label white card12-label3-position">
            <p id="card12-text3" class="font-small">{{ $t('V3C12L4') }}</p>
        </div>
        <div id="card12-label4" class="horizontal-center label white card12-label4-position">
            <p id="card12-text4" class="font-small">{{ $t('V3C12L5') }}</p>
        </div>
        <template v-slot:back-content>
            <div id="card12-back-label1" class="label set-one">
                <p id="card12-back-text1">{{ $t('V3C0L0') + ' ' + "2"}}</p>
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
.card12-label1-position {
    top: calc(191px * var(--scale-factor));
    left: calc(17px * var(--scale-factor));
    width: calc(105px * var(--scale-factor));
    height: calc(20px * var(--scale-factor));
    /* font-size: calc(68px * var(--scale-factor)); */
    text-align: right;
    /* border: solid red 0.5px; */
}

.card12-label1-position p {
    font-weight: 600;
    font-family: "IBM Plex Sans Condensed", sans-serif;
    color : #3573ba;
}

.card12-label2-position {
    top: calc(300px * var(--scale-factor));
    left: calc(17px * var(--scale-factor));
    width: calc(105px * var(--scale-factor));
    height: calc(20px * var(--scale-factor));
    text-align: right;
    /* border: solid red 0.5px; */
}

.card12-label2-position p {
    font-weight: 600;
    font-family: "IBM Plex Sans Condensed", sans-serif;
    color : white;
}

.card12-label3-position {
    top: calc(186px * var(--scale-factor));
    left: calc(246px * var(--scale-factor));
    width: calc(105px * var(--scale-factor));
    height: calc(20px * var(--scale-factor));
    text-align: right;
    /* border: solid red 0.5px; */
}

.card12-label3-position p {
    font-weight: 600;
    font-family: "IBM Plex Sans Condensed", sans-serif;
    color : #3573ba;
;
}

.card12-label4-position {
    top: calc(300px * var(--scale-factor));
    left: calc(320px * var(--scale-factor));
    width: calc(105px * var(--scale-factor));
    height: calc(20px * var(--scale-factor));
    /* border: solid red 0.5px; */
}

.card12-label4-position p {
    font-weight: 600;
    font-family: "IBM Plex Sans Condensed", sans-serif;
    color : #3573ba;
;
}
</style>