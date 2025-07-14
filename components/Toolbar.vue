<script setup lang="ts">
import { breakpointsTailwind, useBreakpoints } from '@vueuse/core'

const breakpoints = useBreakpoints(breakpointsTailwind)

const largerThanLg = breakpoints.greater('lg')

const items = [
	{
		text: 'tmsConnect™',
		icon: 'system-uicons:unlink-horizontal',
		colorOverride: true
	},
	{ text: 'Customers', icon: 'system-uicons:face-happy' },
	{ text: 'Contact', icon: 'system-uicons:paper-plane-alt' },
	{ text: 'About', icon: 'system-uicons:book' }
]
</script>

<template>
	<div
		class="flex items-center justify-between gap-5 p-5 bg-white fixed w-full z-10"
	>
		<div>
			<img
				src="https://reconex.io/wp-content/uploads/2025/01/reconex-loto-dark.svg"
				alt="Logo"
				class="w-[150px] min-w-[150px] h-auto object-contain"
			/>
		</div>
		<div class="flex items-center gap-5">
			<template v-if="largerThanLg">
				<nuxt-link
					v-for="(item, index) in items"
					:key="index"
					:class="[
						'flex items-center gap-1 cursor-pointer text-lg font-medium'
					]"
				>
					<UIcon
						:name="item.icon"
						:class="[
							'size-6 inline-block',
							item.colorOverride ? 'text-[#C80003]' : ''
						]"
					/>
					<div>
						{{ item.text }}
					</div>
				</nuxt-link>
				<UButton
					size="xl"
					:ui="{
						base: 'bg-[#C80003] hover:bg-[#A70002] text-white whitespace-nowrap'
					}"
					trailing-icon="lucide:square-dashed-mouse-pointer"
				>
					Book a demo
				</UButton>
			</template>
			<template v-else>
				<UButton
					size="xl"
					color="neutral"
					trailing-icon="lucide:menu"
					:ui="{ base: 'text-gray-700' }"
					class="!p-2 !rounded-full"
				/>
			</template>
		</div>
	</div>
</template>
