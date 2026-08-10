<script setup lang="ts">
import type { Student } from '@/types'

defineProps<{
  student: Student
}>()
</script>

<template>
  <div class="flex justify-center">
    <div
      class="cursor-pointer border border-[#39495c] p-[20px] w-[250px] mb-[18px] hover:scale-101 hover:shadow-sp"
    >
      <h2>{{ student.name }} {{ student.surname }}</h2>
      <span>GPA: {{ student.gpa }}</span>
    </div>
  </div>
</template>