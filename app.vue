<script setup lang="ts">
const darkMode = ref(false);
</script>

<template>
	<div :class="{ dark: darkMode }">
		<div class="min-h-full">
			<div
				class="grid grid-cols-12 mx-auto sm:px-6 lg:max-w-7xl lg:px-8 lg:gap-5"
			>
				<!-- left sidebar -->
			</div>
		</div>

		<h1 class="text-red-500 dark:text-dim-500">Twitter clone</h1>
	</div>
</template>
