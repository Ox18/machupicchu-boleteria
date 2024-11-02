<script lang="ts" setup></script>

<template>
    <footer class="footer-page">
        <div class="footer-page__logo">
            <img src="@/assets/images/logo-mc.png" alt="ministerio de cultura" height="35" />
        </div>
        <div>
            Sede central Av. Javier Prado Este n° 2465, San Borja, Lima - Perú
        </div>
        <div class="footer-page__logos">
            <img src="@/assets/images/logo-ponle-punche.png" alt="bicentenario perú" height="60" />
            <img src="@/assets/images/logo-bicentenario.svg" alt="bicentenario perú" height="60" />
        </div>
    </footer>
</template>
<style scoped>
.footer-page {
    background-color: #0017fb;
    height: 120px;
    display: flex;
    align-items: center;
    padding-left: 40px;
    padding-right: 40px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    color: #fff;
}

.footer-page__logo {
    border: 1px solid #fff;
    height: 37px;
}

.footer-page__logos {
    display: flex;
    gap: 10px;
}
</style>
