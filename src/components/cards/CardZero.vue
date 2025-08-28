<template>
    <section data-background-size="cover">
        <div class="container">
            <div id="card0-label0" class="label black card0-label0-position">
                <p id="card0-text0">{{ $t('V3C0L3') }}</p>
            </div>
            <div id="card0-label1" v-text-align class="label black card0-label1-position">
                <p id="card0-text1">{{$t('V3C0L5')}}</p>
            </div>
            <div class="label white front-card-label2-position">
                <p>{{ "Climate Fresk - " + $t('V3C0L1') + " - " + $t('V3C0L2') + " - 20/08/2025"}}</p>
            </div>
            <div class="label logo-container-zero">
                <div class="logo"></div>
            </div>
             <div class="label cc-container">
                <div class="cc"></div>
            </div>
            <div class="label qr-code-siteweb-container">
                <div class="qr-code-siteweb"></div>
            </div>
            <div class="label frame-container">
                <div class="frame"></div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: "CardOne",
    data() {
        return {
            imageType: process.env.VUE_APP_IMAGE_TYPE || "png",
        };
    },
};
</script>

<!-- pour une résolution de 470x693 -->
<style>
.card0-label0-position p{
    color : black;
}
.card0-label1-position p{
    color : black;
}

.card0-label0-position {
    top: calc(46px * var(--scale-factor-height));
    left: calc(45.7px * var(--scale-factor-width));
    width: calc(214px * var(--scale-factor-width));
    height: calc(220px * var(--scale-factor-height));
    text-align: left;
    /* border: red solid 0.5px; */
    font-size: calc(40px * var(--scale-factor));
}

.card0-label1-position {
    top: calc(328px * var(--scale-factor-height));
    left: calc(117px * var(--scale-factor-width));
    width: calc(143px * var(--scale-factor-width));
    height: calc(20px * var(--scale-factor-height));
    text-align: center;
    /* border: red solid 0.5px; */
}

.logo-container-zero {
    top: calc(270px * var(--scale-factor-height));
    left: calc(112px * var(--scale-factor-width));
    width: calc(155px * var(--scale-factor-width));
    height: calc(58px * var(--scale-factor-height));
}

.cc {
    width: 100%;
    height: 100%;
    background-image: url('@/assets/creative-commons.png');
    background-size: contain;
}

.cc-container {
    top: calc(146px * var(--scale-factor-height));
    left: calc(263px * var(--scale-factor-width));
    width: calc(80px * var(--scale-factor-width));
    height: calc(29px * var(--scale-factor-height));
}

.qr-code-siteweb {
    width: 100%;
    height: 100%;
    background-image: url('@/assets/qr-code/qr-siteweb-en.png');
    background-size: contain;
}

.qr-code-siteweb-container {
    top: calc(60px * var(--scale-factor-height));
    left: calc(269px * var(--scale-factor-width));
    width: calc(70px * var(--scale-factor-width));
    height: calc(70px * var(--scale-factor-height));
}

</style>