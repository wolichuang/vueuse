<script setup lang="ts">
import { useCycleList } from './index'

const list = [
  'Dog',
  'Cat',
  'Lizard',
  'Shark',
  'Whale',
  'Dolphin',
  'Octopus',
  'Seal',
]

const { state, next, prev } = useCycleList(list)
</script>

<template>
  <div>
    <div class="text-primary text-lg font-bold">
      {{ state }}
    </div>
    <button @click="prev()">
      Prev
    </button>
    <button @click="next()">
      Next
    </button>
  </div>
</template>
