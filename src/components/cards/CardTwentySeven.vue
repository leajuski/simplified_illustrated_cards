<template>
    <CardBase :title="$t('V3C27L0')" :content="$t('V3C27L1')" :card-number="27" :background-front-image="`C27.${imageType}`">
        <div id="card27-label1" class="horizontal-center label card27-label1-position">
        <p id="card27-text1" class="font-small">{{ $t('V3C27L2') }}</p>
        </div>
        <div id="card27-label2" class="horizontal-center label card27-label2-position">
            <p id="card27-text2" class="font-small">{{ $t('V3C27L3') }}</p>
        </div>
        <div id="card27-label3" class="horizontal-center label card27-label3-position">
            <p id="card27-text3" class="font-small">{{ $t('V3C27L4') }}</p>
        </div>
        <template v-slot:back-content>
            <div id="card27-back-label1" class="label set-one">
                <p id="card27-back-text1">{{ $t('V3C0L0') + ' ' + "4"}}</p>
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
.card27-label1-position {
    top: calc(137px * var(--scale-factor));
    left: calc(290px * var(--scale-factor));
    width: calc(105px * var(--scale-factor));
    height: calc(39px * var(--scale-factor));
    font-size: calc(15px * var(--scale-factor));
    /* border: solid red 0.5px; */
    text-align: left;
}

.card27-label1-position p {
    font-weight: 600;
    font-family: "IBM Plex Sans Condensed", sans-serif;
    color : #d35b28;
}

.card27-label2-position {
    top: calc(199px * var(--scale-factor));
    left: calc(290px * var(--scale-factor));
    width: calc(105px * var(--scale-factor));
    height: calc(39px * var(--scale-factor));
    font-size: calc(15px * var(--scale-factor));
    text-align: left;
    /* border: solid red 0.5px; */
}

.card27-label2-position p {
    font-weight: 600;
    font-family: "IBM Plex Sans Condensed", sans-serif;
    color : #d35b28;
}

.card27-label3-position {
    top: calc(330px * var(--scale-factor));
    left: calc(12px * var(--scale-factor));
    width: calc(130px * var(--scale-factor));
    height: calc(39px * var(--scale-factor));
    text-align: left;
    /* border: solid red 0.5px; */
}

.card27-label3-position p {
    font-weight: 600;
    font-family: "IBM Plex Sans Condensed", sans-serif;
    color : #d35b28;
;
}

</style>