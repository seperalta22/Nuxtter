<script lang="ts" setup>
const { defaultTransition: transition } = useTailwindConfig();
</script>

<template>
	<div class="flex flex-col h-screen">
		<div
			class="p-2 my-2 ml-4 hover:bg-blue-50 rounded-full w-min dark:hover:bg-white/20"
			:class="transition"
		>
			<NuxtLink to="/">
				<div class="w-8 h-8">
					<LogoTwitter />
				</div>
			</NuxtLink>
		</div>
		<div class="mt-2 space-y-2">
			<SidebarLeftTab active>
				<template v-slot:icon>
					<Icon name="heroicons:home-20-solid" />
				</template>
				<template #name><p>Home</p></template>
			</SidebarLeftTab>

			<SidebarLeftTab active>
				<template v-slot:icon>
					<Icon name="heroicons:hashtag-20-solid" />
				</template>
				<template #name><p>Explore</p></template>
			</SidebarLeftTab>
			<SidebarLeftTab active>
				<template v-slot:icon>
					<Icon name="heroicons:bell" />
				</template>
				<template #name><p>Notifications</p></template>
			</SidebarLeftTab>
			<SidebarLeftTab active>
				<template v-slot:icon>
					<Icon name="tabler:mail" />
				</template>
				<template #name><p>Messages</p></template>
			</SidebarLeftTab>
			<SidebarLeftTab active>
				<template v-slot:icon>
					<Icon name="ri:bookmark-line" />
				</template>
				<template #name><p>Bookmarks</p></template>
			</SidebarLeftTab>
			<SidebarLeftTab active>
				<template v-slot:icon>
					<div class="w-8 h-8">
						<IconList />
					</div>
				</template>
				<template #name><p>Lists</p></template>
			</SidebarLeftTab>
			<SidebarLeftTab active>
				<template v-slot:icon>
					<div class="w-8 h-8">
						<IconProfile />
					</div>
				</template>
				<template #name><p>Profile</p></template>
			</SidebarLeftTab>
			<SidebarLeftTab active>
				<template v-slot:icon>
					<div class="w-8 h-8">
						<IconDotsOutline />
					</div>
				</template>
				<template #name><p>More</p></template>
			</SidebarLeftTab>
		</div>
	</div>
</template>
