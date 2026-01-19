<template>
    <section data-background-size="cover">
        <div class="container">
            <div id="card28-label0" class="label title card0-label0-position">
                <h1 id="card28-text0">{{ $t('V3C28L0') }}</h1>
            </div>
            <div class="label qr-code-key-container">
                <div class="qr-code-key"></div>
            </div>
        </div>
    </section>
</template>

<script>
</script>

<!-- pour une résolution de 470x693 -->
<style>

.card0-label1-position {
    top: calc(100px * var(--scale-factor-height));
    left: calc(40px * var(--scale-factor-width));
    width: calc(318px * var(--scale-factor-width));
    height: calc(250px * var(--scale-factor-height));
    text-align: left;
    /* border: red solid 0.5px; */
}

.qr-code-key {
    width: 100%;
    height: 100%;
    background-image: url('@/assets/qr-code/qr-code-key.png');
    background-size: contain;
}

.qr-code-key-container {
    top: calc(90px * var(--scale-factor));
    left: calc(73px * var(--scale-factor));
    width: calc(249px * var(--scale-factor));
    height: calc(249px * var(--scale-factor));
}

</style>
