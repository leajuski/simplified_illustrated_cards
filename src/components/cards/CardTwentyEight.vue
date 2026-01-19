<template>
    <section data-background-size="cover">
        <div class="container">
            <div id="card28-label0" class="label title">
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

.qr-code-key {
    width: 100%;
    height: 100%;
    background-image: url('@/assets/qr-code/qr-code-key-fr.png');
    background-size: contain;
}

.qr-code-key-container {
    top: calc(90px * var(--scale-factor));
    left: calc(73px * var(--scale-factor));
    width: calc(249px * var(--scale-factor));
    height: calc(249px * var(--scale-factor));
}

</style>
