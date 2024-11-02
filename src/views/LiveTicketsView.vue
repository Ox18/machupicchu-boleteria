<script setup lang="ts">
import TicketPreview from '@/components/TicketPreview/TicketPreview.vue'
import TicketPreviewLayout from '@/components/layouts/TicketPreviewLayout.vue'
import ClockTimer from '@/components/ClockTimer.vue'
import BoxComponent from '@/components/BoxComponent.vue'
</script>
<template>
  <main class="live-tickets-view">
    <div class="live-tickets-view__content">
      <div class="clock-timer">
        <BoxComponent variant="red">
          <h2>Centro Cultural</h2>
        </BoxComponent>
        <div></div>
        <BoxComponent>
          <ClockTimer />
        </BoxComponent>
      </div>
      <div class="live-tickets-view__preview">
        <TicketPreviewLayout>
          <TicketPreview title="Ruta 1-A: Montaña Machupicchu" :aforo="100" :vendidos="50" :disponibles="50" />
          <TicketPreview title="Ruta 1-B: Terraza Superior" :aforo="100" :vendidos="50" :disponibles="50" />
          <TicketPreview title="Ruta 2-A: Clásico Diseñada" :aforo="100" :vendidos="50" :disponibles="50" />
          <TicketPreview title="Ruta 2-B: Terraza Superior" :aforo="100" :vendidos="50" :disponibles="50" />
          <TicketPreview title="Ruta 3-A: Montaña Wayna Picchu" :aforo="100" :vendidos="50" :disponibles="50" />
          <TicketPreview title="Ruta 3-B: Realeza diseñada" :aforo="100" :vendidos="50" :disponibles="50" />
        </TicketPreviewLayout>
      </div>
    </div>
  </main>
</template>
<style scoped>
.live-tickets-view {
  padding-top: 20px;
  background-color: #f0f0f0;
  background-image: url(../assets/images/machu-picchu.png);
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  display: flex;
  justify-content: center;
}

.live-tickets-view__preview {
  margin-top: 10px;
  margin-bottom: 10px;
}

.live-tickets-view__content {
  width: 80%;
}

.clock-timer {
  margin-bottom: 40px;
  display: grid;
  grid-template-columns: auto 1fr auto;
  justify-content: space-between;
  align-items: center;
  gap: 20px;
}
</style>
