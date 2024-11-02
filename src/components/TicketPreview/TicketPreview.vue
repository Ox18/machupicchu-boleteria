<script setup lang="ts">
import TicketPreviewCounter from './TicketPreviewCounter.vue'

defineProps({
    title: String,
    aforo: Number,
    vendidos: Number,
    disponibles: Number,
})
</script>
<template>
    <div class="ticket-preview">
        <h2 class="ticket-preview__title">
            {{ title }}
        </h2>
        <div class="ticket-preview__info">
            <TicketPreviewCounter :value="aforo" label="aforo" />
            <TicketPreviewCounter :value="vendidos" label="vendidos" variant="red" />
            <TicketPreviewCounter :value="disponibles" label="disponibles" variant="cian" />
        </div>
    </div>
</template>
<style scoped>
.ticket-preview {
    background-color: var(--color-blue-dark);
    border-radius: 7px;
    padding: 10px;
    color: #fff;
    display: flex;
    flex-direction: column;
}

.ticket-preview__title {
    font-weight: bold;
    text-align: center;
}

.ticket-preview__info {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    margin-top: 10px;
    gap: 5px;
}
</style>
