<template>
    <div class="ticket-preview-layout">
        <slot></slot>
    </div>
</template>

<style scoped>
.ticket-preview-layout {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 10px;
    align-items: center;
    justify-content: center;

    @media (max-width: 768px) {
        grid-template-columns: 1fr;
    }

    @media (max-width: 1024px) {
        grid-template-columns: 1fr;
    }
}
</style>
