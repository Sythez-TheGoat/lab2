<script setup lang="ts">
import type { Event } from '@/types'

defineProps<{
  event: Event
}>()
</script>

<template>
  <div class="event-meta">
    <span>{{ event.category }}</span>
    <span>{{ event.organizer }}</span>
  </div>
</template>
<script setup lang="ts">
import type { Event } from '@/types'

defineProps<{
  event: Event
}>()
</script>

<template>
  <div class="flex flex-col items-end text-sm">
    <span>{{ event.category }}</span>
    <span>{{ event.organizer }}</span>
  </div>
</template>
<style scoped>
.event-meta {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  font-size: 14px;
}
</style>