<template>
    <section :style="backgroundStyles">
        <div class="container">
            <div :id="`card${cardNumber}-label0`" class="label title">
                <h1 :id="`card${cardNumber}-text0`">{{ title }}</h1>
            </div>
            <!-- <hr class="label border-white top-left-vertical">
            <hr class="label border-white top-left-horizontal">
            <hr class="label border-white top-right-vertical">
            <hr class="label border-white top-right-horizontal">
            <hr class="label border-white bottom-left-vertical">
            <hr class="label border-white bottom-left-horizontal">
            <hr class="label border-white bottom-right-vertical">
            <hr class="label border-white bottom-right-horizontal"> -->
            <slot></slot>
        </div>
    </section>
    <section>
        <div class="container">
            <!-- <div :id="`card${cardNumber}-label0`" class="label black title">
                <h1 :id="`card${cardNumber}-text0`">{{ title }}</h1>
            </div> -->
            <div :id="`card${cardNumber}-titleback-label0`" class="label black title">
                <h1 :id="`card${cardNumber}-titleback-text0`">{{ title }}</h1>
            </div>
            <div :id="`card${cardNumber}-back-label0`" class="label black content">
                <p :id="`card${cardNumber}-back-text0`">{{ content }}</p>
            </div>
            <div class="label logo-container">
                <div class="logo"></div>
            </div>
            <!-- <hr class="label border-black top-left-vertical">
            <hr class="label border-black top-left-horizontal">
            <hr class="label border-black top-right-vertical">
            <hr class="label border-black top-right-horizontal">
            <hr class="label border-black bottom-left-vertical">
            <hr class="label border-black bottom-left-horizontal">
            <hr class="label border-black bottom-right-vertical">
            <hr class="label border-black bottom-right-horizontal"> -->
            <slot name="back-content"></slot>
        </div>
    </section>
</template>


<script>
export default {
    name: "CardBase",
    props: {
        backgroundFrontImage: {
            type: String,
            required: true,
        },
        cardNumber: {
            type: Number,
            required: true,
        },
        title: {
            type: String,
            required: true,
        },
        content: {
            type: String,
            required: true,
        },
    },
    data() {
        return {
            imageType: process.env.VUE_APP_IMAGE_TYPE || "png",
            mini: process.env.VUE_APP_MINI === 'true',
        };
    },
    computed: {
        backgroundFrontImageUrl() {
            return require(`@/assets/${this.imageType}/${this.backgroundFrontImage}`);
        },
        backgroundStyles() {
            if (this.mini) { 
                return {
                    backgroundImage: `url(${this.backgroundFrontImageUrl})`,
                    backgroundSize: 'cover',
                    backgroundPosition: 'top left',
                    position: 'absolute',
                    top: '8px',
                    left: '8px',
                    width: '411px', // Pour occuper toute la largeur de la section parente
                    height: '279px', // Pour occuper toute la hauteur de la section parente
                };
            } else {
                return {
                    backgroundImage: `url(${this.backgroundFrontImageUrl})`,
                    backgroundSize: 'cover',
                    backgroundPosition: 'top left',
                    position: 'absolute',
                    top: '0px',
                    left: '0px',
                    width: '100%',
                    height: '100%',
                };
            } 
        },
    },
};

</script>

<style>
.container {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    font-weight: 500;
}

.background {
    position: absolute;
    top: 20px;
    left: 20px;
    width: 423px;
    height: 291px;
}

.title {
    /* border: solid red 0.5px; */
    top: calc(40px * var(--scale-factor-height));
    left: calc(40px * var(--scale-factor-width));
    width: calc(318px * var(--scale-factor-width));
    height: calc(60px * var(--scale-factor-height));
    text-align: left;

}

.content {
    /* border: solid red 0.5px; */
    top: calc(100px * var(--scale-factor-height));
    left: calc(40px * var(--scale-factor-width));
    width: calc(318px * var(--scale-factor-width));
    height: calc(190px * var(--scale-factor-height));
    text-align: left;
    line-height: 12px; 
}

.title h1 {
    font-size: calc(23px * var(--scale-factor));
}

.content p {
    /* font-size: calc(256px * var(--scale-factor)); */
    font-size: calc(20px * var(--scale-factor));
}

/* default is en logo */
.logo-container {
    top: calc(330px * var(--scale-factor-height));
    left: calc(281px * var(--scale-factor-width));
    width: calc(80px * var(--scale-factor-width));
    height: calc(31px * var(--scale-factor-height));
}

.logo {
    width: 100%;
    height: 100%;
    background-image: url('@/assets/logo-en.png');
    background-size: contain;
}

.url {
    font-size: calc(16.3px * var(--scale-factor));
}

.back-set-container {
    /* border: solid red; */
    top: calc(25px * var(--scale-factor-height));
    left: calc(30.2px * var(--scale-factor-width));
    width: calc(76.5px * var(--scale-factor-width));
    height: calc(82px * var(--scale-factor-height));
}

.front-set-container {
    /* border: solid red; */
    top: calc(306px * var(--scale-factor-height));
    left: calc(23.2px * var(--scale-factor-width));
    width: calc(73.1px * var(--scale-factor-width));
    height: calc(79px * var(--scale-factor-height));
}

.card-number {
    z-index: 4;
    font-size: calc(34px * var(--scale-factor));
}


.set-one {
    top: calc(327px * var(--scale-factor-height));
    left: calc(40px * var(--scale-factor-width));
    width: calc(120px * var(--scale-factor-width));
    height: calc(32px * var(--scale-factor-height));
    font-weight: 500;
    font-size: calc(30px * var(--scale-factor));
    /* border: red solid 1px; */
    display: flex;
    align-items: center;
}

.set-one p {
    font-family: "IBM Plex Sans Condensed", sans-serif;
    font-weight: 600;
    color : black;
    text-align: left;
}

.set-two {
    top: calc(340.5px * var(--scale-factor-height));
    left: calc(138.5px * var(--scale-factor-width));
    width: calc(100px * var(--scale-factor-width));
    height: calc(70px * var(--scale-factor-height));
    background-color: red;
    padding-top: calc(9.5px * var(--scale-factor));
    font-weight: 430;
    font-size: calc(19px * var(--scale-factor));
}

.set-three {
    top: calc(340.5px * var(--scale-factor-height));
    left: calc(248.5px * var(--scale-factor-width));
    width: calc(100px * var(--scale-factor-width));
    height: calc(70px * var(--scale-factor-height));
    background-color: red;
    padding-top: calc(9.5px * var(--scale-factor));
    font-weight: 430;
    font-size: calc(19px * var(--scale-factor));
}

.set-four {
    top: calc(340.5px * var(--scale-factor-height));
    left: calc(358.6px * var(--scale-factor-width));
    width: calc(100px * var(--scale-factor-width));
    height: calc(70px * var(--scale-factor-height));
    background-color: red;
    padding-top: calc(9.5px * var(--scale-factor));
    font-weight: 430;
    font-size: calc(19px * var(--scale-factor));
}

.set-five {
    top: calc(340.5px * var(--scale-factor-height));
    left: calc(469px * var(--scale-factor-width));
    width: calc(100px * var(--scale-factor-width));
    height: calc(70px * var(--scale-factor-height));
    background-color: red;
    padding-top: calc(9.5px * var(--scale-factor));
    font-weight: 430;
    font-size: calc(19px * var(--scale-factor));
}

.set p {
    font-size: calc(134px * var(--scale-factor));
}
</style>