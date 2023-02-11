<script lang="ts" setup>
const { defaultTransition: transition } = useTailwindConfig();

const props = defineProps({
	active: {
		type: Boolean,
		default: false,
	},
});

const textClasses = computed(() =>
	props.active ? 'font-bold' : 'font-medium'
);
</script>

<template>
	<NuxtLink
		to="#"
		class="flex items-center p-4 hover:bg-gray-200 rounded-full w-min dark:hover:bg-dim-200 dark:text-white text-black"
		:class="transition"
	>
		<div class="w-10 text-black ml-2 dark:text-white">
			<slot name="icon"></slot>
		</div>

		<div class="ml-4 mr-4 text-xl hidden xl:block" :class="textClasses">
			<slot name="name"></slot>
		</div>
	</NuxtLink>
</template>
