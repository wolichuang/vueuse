# 使用
<template>
	<div>sourceType: {{sourceType}} x: {{ x }} y: {{ y }}</div>
</template>
<script type="ts">
// import { reactive } from 'vue' 
import { debounceFilter, useMouse } from '@vueuse/core'

export default {
	setup() {
		const { x, y, sourceType} = useMouse({ eventFilter: debounceFilter(100) });
		return {x, y,sourceType};
	}
}
</script>