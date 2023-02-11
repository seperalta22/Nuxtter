<script setup lang="ts">
const props = defineProps<{
	title: string;
}>();
</script>

<template>
	<h3>
		{{ props.title }}
	</h3>
</template>
