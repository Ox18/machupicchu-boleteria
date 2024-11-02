<script setup lang="ts"></script>
<template>
    <div class="main-layout">
        <slot></slot>
    </div>
</template>
<style scoped>
.main-layout {
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: auto 1fr auto;
    height: 100vh;
}
</style>
