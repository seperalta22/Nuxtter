<script setup lang="ts">
const darkMode = ref(true);
</script>

<template>
	<div :class="{ dark: darkMode }">
		<div class="bg-white dark:bg-dim-900 dark:text-white">
			<div class="min-h-full">
				<div
					class="grid grid-cols-12 mx-auto sm:px-6 lg:max-w-7xl lg:px-8 lg:gap-5"
				>
					<!--! left Sidebar -->
					<div
						class="xs:block col-span-2 md:col-span-1 xl:col-span-3 border-2 border-red-500"
					>
						<div class="sticky top-0">
							<SidebarLeft />
						</div>
					</div>

					<!--! Main Content -->

					<main
						class="col-span-10 bg-red-500 md:col-span-8 xl:col-span-6"
					>
						<h1>Asd</h1>
					</main>

					<!--! Right Sidebar -->

					<div class="hidden md:block xl:col-span-3 md:col-span-2">
						<div class="sticky top-0">
							<SidebarRight />
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>
