<script setup lang="ts">
import { ref } from 'vue-demi'
import { onStartTyping } from '.'

const input = ref<HTMLInputElement | null>(null)

onStartTyping(() => {
  if (!input.value?.active)
    input.value!.focus()
})
</script>

<template>
  <note>Type anything</note>
  <input ref="input" type="text" placeholder="Start typing to focus">
  <input type="text" placeholder="Start typing has no effect here">
</template>
