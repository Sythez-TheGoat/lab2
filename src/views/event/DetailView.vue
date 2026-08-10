<script setup lang="ts">
import { toRefs } from 'vue'
import { storeToRefs } from 'pinia'
import { useMessageStore } from '@/stores/message'
import type { Event } from '@/types'

const props = defineProps<{
  event: Event
}>()

const { event } = toRefs(props)

const store = useMessageStore()
const { message } = storeToRefs(store)
</script>

<template>
  <div id="flashMessage" class="animate-fade" v-if="message">
    <h4>{{ message }}</h4>
  </div>
  <p>{{ event.time }} on {{ event.date }} @ {{ event.location }}</p>
  <p>{{ event.description }}</p>
</template>