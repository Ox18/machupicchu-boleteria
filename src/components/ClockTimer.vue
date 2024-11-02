<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue'

const time = ref(new Date().toLocaleTimeString())
const ampm = ref('')

defineProps({
    visibleDate: {
        type: Boolean,
        default: true,
    },
})

const date = ref(new Date().toLocaleDateString())

const hours = ref(new Date().getHours())

const minutes = ref(new Date().getMinutes().toString())

onMounted(() => {
    const timer = setInterval(() => {
        time.value = new Date().toLocaleTimeString()

        const hours_f = new Date().getHours()

        if (hours_f >= 12) {
            ampm.value = 'PM'
        } else {
            ampm.value = 'AM'
        }

        hours.value = hours_f
        const minutes_f = new Date().getMinutes()

        if (minutes_f < 10) {
            minutes.value = `0${minutes_f}`
        } else {
            minutes.value = minutes_f.toString()
        }
    }, 1000)
    onUnmounted(() => {
        clearInterval(timer)
    })
})
</script>

<template>
    <h2>
        {{ visibleDate ? `${date}` : '' }}

        {{ hours }}:{{ minutes }}
        {{ ampm }}
    </h2>
</template>
