<script setup lang="ts">
defineProps({
    variant: String,
})
</script>
<template>
    <div :class="`box box__variant-${variant}`">
        <slot></slot>
    </div>
</template>
<style scoped>
.box {
    padding: 10px;
    border-radius: 10px;
    margin-bottom: 20px;
}

.box__variant-red {
    background-color: var(--color-red);
    color: #fff;
}

.box__variant-blue {
    background-color: var(--color-blue);
}
</style>
