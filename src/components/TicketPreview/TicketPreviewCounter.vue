<script setup lang="ts">
import { computed } from 'vue'

const props = defineProps({
    label: String,
    value: Number,
    variant: String,
})

const classVariant = computed(() => {
    return `ticket-preview-counter__value--${props.variant}`
})
</script>

<template>
    <div class="ticket-preview-counter" :class="classVariant">
        <h2 class="ticket-preview-counter__value">
            {{ value }}
        </h2>
        <label class="ticket-preview-counter__label">
            {{ label }}
        </label>
    </div>
</template>
<style scoped>
.ticket-preview-counter {
    display: flex;
    border: 2px solid var(--color-white);
    padding: 15px;
    border-radius: 7px;
    align-items: center;
    justify-content: center;

    flex-wrap: wrap;
    align-items: center;
}

.ticket-preview-counter__value {
    font-size: 1.5rem;
    margin-right: 10px;
    font-weight: bold;
}

.ticket-preview-counter__label {
    text-transform: uppercase;
}

.ticket-preview-counter__value--red {
    color: var(--color-red);
}

.ticket-preview-counter__value--cian {
    color: var(--color-cian);
}
</style>
