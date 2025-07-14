<script setup lang="ts">
import type { BreadcrumbItem } from '@nuxt/ui'

const items = ref<BreadcrumbItem[]>([
	{
		label: 'Home',
		icon: 'i-lucide-house'
	},
	{
		label: 'Dashboard',
		icon: 'i-lucide-grid',
		to: '/dashboard'
	}
])
</script>

<template>
	<div class="flex flex-col h-full">
		<Toolbar />
		<section class="mt-[64px]">
			<div class="overflow-hidden bg-white py-8 lg:py-24">
				<div class="mx-auto max-w-7xl px-8">
					<div
						class="mx-auto grid max-w-2xl grid-cols-1 gap-x-8 gap-y-16 sm:gap-y-20 lg:mx-0 lg:max-w-none lg:grid-cols-2"
					>
						<div class="flex">
							<div class="lg:max-w-lg my-auto">
								<p
									class="mt-8 text-4xl sm:text-5xl font-black tracking-tight text-pretty text-gray-900"
								>
									See every load. Zero tab chaos.
								</p>
								<p class="my-8 text-lg/8 text-gray-700">
									See performance, damage, delays, and missed
									pickups, down to the shipment. Compare your
									carriers to tmsConnect™ benchmarks and flag
									the slackers.
								</p>
								<dl class="flex gap-2.5 max-w-xl">
									<UButton
										size="xl"
										color="neutral"
										trailing-icon="lucide:info"
									>
										Learn more
									</UButton>
									<UButton
										size="xl"
										:ui="{
											base: 'bg-[#C80003] hover:bg-[#A70002] text-white'
										}"
										trailing-icon="lucide:square-dashed-mouse-pointer"
									>
										Book a demo
									</UButton>
								</dl>
							</div>
						</div>

						<img
							src="https://reconex.io/wp-content/uploads/2025/05/carrier-performance-dash.svg"
							alt="Product screenshot"
							class="w-3xl max-w-none rounded-xl shadow-xl ring-1 ring-gray-400/10 sm:w-228 md:-ml-4 lg:-ml-0"
							width="2432"
							height="1442"
						/>
					</div>
				</div>
			</div>
		</section>

		<section class="bg-white py-8 sm:py-24">
			<div class="mx-auto max-w-7xl px-6 lg:px-8">
				<h2 class="text-center text-2xl font-semibold text-gray-900">
					<span class="font-black">Trusted</span>
					by freight hustlers.
					<span class="font-black">Built</span>
					for the grind.
				</h2>
				<div
					class="mx-auto mt-10 grid max-w-lg grid-cols-4 items-center gap-x-8 gap-y-10 sm:max-w-xl sm:grid-cols-6 sm:gap-x-10 lg:mx-0 lg:max-w-none lg:grid-cols-5"
				>
					<img
						class="col-span-2 max-h-12 w-full object-contain lg:col-span-1"
						src="https://reconex.io/wp-content/uploads/2025/01/la-z-boy-svg.svg"
						alt="La-Z-Boy"
						width="158"
						height="48"
					/>

					<img
						class="col-span-2 max-h-12 w-full object-contain lg:col-span-1"
						src="https://reconex.io/wp-content/uploads/2025/01/kerma-medical-svg.svg"
						alt="Kerma Medical"
						width="158"
						height="48"
					/>

					<img
						class="col-span-2 max-h-12 w-full object-contain lg:col-span-1"
						src="https://reconex.io/wp-content/uploads/2025/01/cleveland-steel-container-svg.svg"
						alt="Cleveland Steel Container"
						width="158"
						height="48"
					/>

					<img
						class="col-span-2 max-h-12 w-full object-contain sm:col-start-2 lg:col-span-1"
						src="https://reconex.io/wp-content/uploads/2025/01/jovial-foods-svg.svg"
						alt="Jovial Foods"
						width="158"
						height="48"
					/>

					<img
						class="col-span-2 col-start-2 max-h-12 w-full object-contain sm:col-start-auto lg:col-span-1"
						src="https://reconex.io/wp-content/uploads/2025/01/wood-mizer-svg.svg"
						alt="Wood-Mizer"
						width="158"
						height="48"
					/>
				</div>
			</div>
		</section>

		<section class="bg-white px-8 py-8 sm:py-12">
			<figure class="mx-auto max-w-2xl">
				<p class="sr-only">5 out of 5 stars</p>
				<div class="flex gap-x-1">
					<UIcon
						name="ic:outline-star"
						class="size-8 flex-none text-yellow-500"
						aria-hidden="true"
					/>
					<UIcon
						name="ic:outline-star"
						class="size-8 flex-none text-yellow-500"
						aria-hidden="true"
					/>
					<UIcon
						name="ic:outline-star"
						class="size-8 flex-none text-yellow-500"
						aria-hidden="true"
					/>
					<UIcon
						name="ic:outline-star"
						class="size-8 flex-none text-yellow-500"
						aria-hidden="true"
					/>
					<UIcon
						name="ic:outline-star"
						class="size-8 flex-none text-yellow-500"
						aria-hidden="true"
					/>
				</div>
				<blockquote
					class="mt-10 text-xl/8 font-light tracking-tight text-gray-900 sm:text-2xl/9"
				>
					<p>
						“All of our processes were manual, and invoice
						reconciliation was a nightmare. We also didn't have the
						ability to rate shop various lanes or perform effective
						audits. Every change we've made has been a win — but the
						best part? Lower prices thanks to our ability to lane
						quote.”
					</p>
				</blockquote>
				<figcaption class="mt-10 flex items-center gap-x-6">
					<div>
						<div class="flex gap-2.5">
							<div class="font-semibold text-gray-900 mt-4">
								Jeff Hurley
							</div>
						</div>
						<div class="mt-0.5 text-gray-600">
							Operations Manager | Kerma Medical Products
						</div>
					</div>
				</figcaption>

				<div class="mt-10">
					<UButton
						color="neutral"
						variant="subtle"
						size="xl"
					>
						Kerma's FS 5000 story.
						<UIcon
							name="lucide:arrow-right"
							class="size-5"
							aria-hidden="true"
						/>
					</UButton>
				</div>
			</figure>
		</section>

		<section class="bg-white px-8 py-12 sm:py-24 text-center">
			<div
				class="text-4xl sm:text-5xl font-black bg-gradient-to-r from-[#111] to-[#C80003] inline-block text-transparent bg-clip-text"
			>
				Real pains. Real results.
			</div>
			<div class="mt-10 text-xl/8 text-gray-700 max-w-2xl mx-auto">
				<p>
					You've lived the chaos! No updates, bogus fees, rate hikes,
					and disconnected systems. It all makes you want to take a
					chainsaw to your old-school 3PL spreadsheet. Shut it all
					down with live data, smart carrier calls, and one platform
					that actually works. Fast. Every time.
				</p>
			</div>
		</section>

		<section class="bg-[#eee] pt-12 sm:pt-24">
			<div class="mx-auto max-w-7xl px-6 lg:px-8">
				<div class="mx-auto max-w-2xl sm:text-center">
					<h2 class="text-2xl font-semibold">
						<strong>One</strong>
						partner.
						<strong>Six</strong>
						core services.
					</h2>

					<div class="mt-10 text-4xl sm:text-5xl font-black">
						<span
							class="bg-gradient-to-r from-[#111] to-[#C80003] text-transparent bg-clip-text"
						>
							The freight system
						</span>
						you'd build if you had time.
					</div>

					<p class="mt-6 text-lg/8">
						Freight gets messy fast. You have disconnected tools,
						missing data, and no visibility. That's why Reconex is
						your complete freight command center.
					</p>

					<p class="mt-6 text-lg/8 font-bold">
						Built to move your freight. Smarter.
					</p>
				</div>
			</div>

			<div class="relative overflow-hidden pt-16">
				<div class="mx-auto max-w-7xl px-6 lg:px-8">
					<div class="flex justify-end">
						<img
							src="https://reconex.io/wp-content/uploads/2025/06/snoop.svg"
							alt="Snoop"
							class="sm:w-[280px] w-[200px] h-auto object-cover"
						/>
					</div>
					<a href="">
						<img
							src="https://reconex.io/wp-content/uploads/2025/05/ops-core.svg"
							alt="App screenshot"
							class="mb-[-12%] rounded-xl shadow-2xl ring-1 ring-white/10 hover:scale-101 transition-transform duration-300 ease-in-out"
							width="2432"
							height="1442"
						/>
					</a>
					<div
						class="relative"
						aria-hidden="true"
					>
						<div
							class="absolute -inset-x-20 bottom-0 bg-linear-to-t from-gray-900 pt-[7%]"
						/>
					</div>
				</div>
			</div>
		</section>

		<section
			class="flex lg:flex-row flex-col items-center gap-10 bg-white py-24 sm:py-32 lg:overflow-visible lg:px-0"
		>
			<div class="lg:w-2/5 px-8">
				<h1
					class="mt-2 text-4xl font-bold tracking-tight text-pretty text-gray-900 sm:text-5xl"
				>
					Live quotes. Zero guesswork.
				</h1>
				<p class="mt-6 text-xl/8 text-gray-700">
					Real-time rating logic gives you everything up front —
					accessorials, insurance, performance, and customer charges.
					Full breakdown, all in one view.
				</p>
			</div>
			<div class="lg:w-3/5 px-8">
				<img
					class="w-full flex-1 max-w-none rounded-xl"
					src="https://reconex.io/wp-content/uploads/2025/05/rate-stack-2.svg"
					alt="Rate stack screenshot"
				/>
			</div>
		</section>

		<section
			class="bg-[#2c2c2c] text-white px-8 py-12 sm:py-24 text-center"
		>
			<div class="text-3xl sm:text-4xl">
				Clients
				<span class="font-black">cut freight costs</span>
				by
				<span class="font-black">23.57%*</span>
				with
				<span class="font-black">RateAlignment™</span>
			</div>
			<UButton
				size="xl"
				:ui="{
					base: 'bg-[#C80003] hover:bg-[#A70002] text-xl text-white whitespace-nowrap p-3'
				}"
				trailing-icon="lucide:arrow-right"
				class="mt-10"
			>
				Lets talk
			</UButton>

			<div class="mt-10">
				<p class="text-sm text-gray-500">
					*Based on client data from 2024. Individual results may
					vary.
				</p>
			</div>
		</section>

		<section class="bg-white px-8 py-8 sm:py-12 text-center">
			<div class="overflow-hidden bg-white py-8 lg:py-24">
				<div class="mx-auto max-w-7xl px-8">
					<div
						class="mx-auto grid max-w-2xl grid-cols-1 gap-x-8 gap-y-16 sm:gap-y-20 lg:mx-0 lg:max-w-none lg:grid-cols-2"
					>
						<div class="flex text-left">
							<div class="lg:max-w-lg my-auto">
								<p
									class="mt-8 text-4xl sm:text-5xl font-bold tracking-tight text-pretty text-gray-900"
								>
									OpsCore™
								</p>
								<p
									class="my-4 sm:text-2xl text-xl text-gray-500 font-bold"
								>
									Your network in motion. Always visible.
								</p>
								<p class="mt-8 text-xl">
									It's your real-time control screen for LTL
									and TL. One view displays every alert,
									exception, delay, and dispatch status as
									they occur. You see what's moving, what's
									stuck, and what needs attention — right now.
									And
									<span class="font-bold">LiveAudit™</span>
									and
									<span class="font-bold">
										GroundControl™
									</span>
									always have your back.
								</p>
							</div>
						</div>

						<img
							src="https://reconex.io/wp-content/uploads/2025/06/tracker.svg"
							alt="Product screenshot"
							class="w-full max-w-none rounded-xl shadow-xl"
						/>
					</div>
				</div>
			</div>
		</section>

		<section class="bg-white px-8 pt-8 pb-16">
			<figure class="mx-auto max-w-2xl">
				<p class="sr-only">5 out of 5 stars</p>
				<div class="flex gap-x-1">
					<UIcon
						name="ic:outline-star"
						class="size-8 flex-none text-yellow-500"
						aria-hidden="true"
					/>
					<UIcon
						name="ic:outline-star"
						class="size-8 flex-none text-yellow-500"
						aria-hidden="true"
					/>
					<UIcon
						name="ic:outline-star"
						class="size-8 flex-none text-yellow-500"
						aria-hidden="true"
					/>
					<UIcon
						name="ic:outline-star"
						class="size-8 flex-none text-yellow-500"
						aria-hidden="true"
					/>
					<UIcon
						name="ic:outline-star"
						class="size-8 flex-none text-yellow-500"
						aria-hidden="true"
					/>
				</div>
				<blockquote
					class="mt-10 text-xl/8 font-light tracking-tight text-gray-900 sm:text-2xl/9"
				>
					<p>
						“Reconex TMS has made the carrier booking process a
						breeze for our plant personnel.”
					</p>
				</blockquote>
				<figcaption class="mt-10 flex items-center gap-x-6">
					<div>
						<div>
							<img
								src="https://reconex.io/wp-content/uploads/2025/05/ICP-Group2.svg"
								alt="ICP Group Logo"
								class="w-10 h-auto object-contain mb-2"
							/>
						</div>
						<div class="flex gap-2.5">
							<div class="font-semibold text-gray-900 mt-4">
								Greg Fischer
							</div>
						</div>
						<div class="mt-0.5 text-gray-600">
							Logistics Manager | ICP Group Inc
						</div>
					</div>
				</figcaption>
			</figure>
		</section>

		<section class="bg-white px-8 py-12 sm:py-24 text-center">
			<div class="text-2xl sm:text-3xl text-[#C80003]">SmartSelect™</div>

			<div class="mt-10 text-4xl sm:text-5xl font-bold">
				Stop guessing.
				<span class="line-through">Start</span>
				Smart selecting.
				<UIcon
					name="lucide:square-check"
					class="inline-block sm:size-8 size-6 text-[#C80003]"
				/>
			</div>

			<div class="mt-10 text-xl/8 text-gray-700 max-w-2xl mx-auto">
				<p>
					SmartSelect™ Stop guessing. Start Smart selecting. Dial in
					exactly how you rate carriers — cost, speed, performance —
					it's your call. Tweak the bias, see how it hits your bottom
					line, and lock in the mix that fits your business. The
					result?
					<span class="font-bold">
						Smarter choices. No guesswork. Every time.
					</span>
				</p>
			</div>
		</section>

		<section class="bg-white px-8 text-center">
			<div class="overflow-hidden bg-white py-8 lg:py-24">
				<div class="mx-auto max-w-7xl px-8">
					<div
						class="mx-auto grid max-w-2xl grid-cols-1 gap-x-8 gap-y-16 sm:gap-y-20 lg:mx-0 lg:max-w-none lg:grid-cols-2"
					>
						<div class="flex text-left">
							<div class="lg:max-w-lg my-auto">
								<p
									class="mt-8 text-4xl sm:text-5xl font-bold tracking-tight text-pretty text-gray-900"
								>
									Performance. Cost. Speed. You rule!
								</p>
								<p class="mt-8 sm:text-xl text-lg">
									Your rules, your logic, your priorities —
									automated into every rate shop and dispatch.
								</p>
								<ul class="flex flex-col gap-4 mt-8">
									<li class="flex gap-4">
										<div>
											<UIcon
												name="lucide:award"
												class="sm:size-8 size-6 text-[#C80003]"
											/>
										</div>
										<div>
											<div class="font-bold">
												Trust the data that carriers
												can't touch
											</div>
											SmartSelect™ runs on Reconex's
											independent performance
											data—unfiltered, unbiased, and built
											in-house. You won't find it anywhere
											else.
										</div>
									</li>
									<li class="flex gap-4">
										<div>
											<UIcon
												name="lucide:square-user-round"
												class="sm:size-8 size-6 text-[#C80003]"
											/>
										</div>
										<div>
											<div class="font-bold">
												Set the standard
											</div>
											Build an executive-led framework
											that drives consistent carrier
											routing and LTL cost control — then
											hold teams accountable to it.
										</div>
									</li>
									<li class="flex gap-4">
										<div>
											<UIcon
												name="lucide:git-branch"
												class="sm:size-8 size-6 text-[#C80003]"
											/>
										</div>
										<div>
											<div class="font-bold">
												Control what works
											</div>
											Apply your 'best-way' rules across
											all locations. Or fine-tune them one
											by one. Total control. Total
											accountability.
										</div>
									</li>
								</ul>
							</div>
						</div>

						<img
							src="https://reconex.io/wp-content/uploads/2025/05/smart-select-2.svg"
							alt="Product screenshot"
							class="w-full max-w-none rounded-xl shadow-xl"
						/>
					</div>
				</div>
			</div>
		</section>

		<section
			class="artboard overlay flex relative bg-white px-8 pt-8 pb-16 bg-cover bg-center bg-no-repeat"
		>
			<div
				class="absolute inset-0 bg-white/75 pointer-events-none z-0"
				aria-hidden="true"
			/>
			<figure class="mx-auto max-w-2xl z-10">
				<p class="sr-only">5 out of 5 stars</p>
				<div class="flex gap-x-1">
					<UIcon
						name="ic:outline-star"
						class="size-8 flex-none text-yellow-500"
						aria-hidden="true"
					/>
					<UIcon
						name="ic:outline-star"
						class="size-8 flex-none text-yellow-500"
						aria-hidden="true"
					/>
					<UIcon
						name="ic:outline-star"
						class="size-8 flex-none text-yellow-500"
						aria-hidden="true"
					/>
					<UIcon
						name="ic:outline-star"
						class="size-8 flex-none text-yellow-500"
						aria-hidden="true"
					/>
					<UIcon
						name="ic:outline-star"
						class="size-8 flex-none text-yellow-500"
						aria-hidden="true"
					/>
				</div>
				<blockquote
					class="mt-10 text-xl/8 font-light tracking-tight text-gray-900 sm:text-2xl/9"
				>
					<p>
						“Do you like to sleep at night knowing that your
						shipments are being managed with the utmost care? Then,
						let Reconex rock you to sleep.”
					</p>
				</blockquote>
				<figcaption class="mt-10 flex items-center gap-x-6">
					<div>
						<div>
							<img
								src="https://reconex.io/wp-content/uploads//2025/02/speedball-logo.svg"
								alt="Speedball Logo"
								class="w-32 h-auto object-contain mb-2"
							/>
						</div>
						<div class="flex gap-2.5">
							<div class="font-semibold text-gray-900 mt-4">
								Maria Barringer
							</div>
						</div>
						<div class="mt-0.5 text-gray-600">
							Director of Supply Chain | Speedball Art Products
						</div>
					</div>
				</figcaption>
			</figure>
		</section>

		<footer
			class="flex sm:flex-row flex-col items-center justify-between p-8 gap-5"
		>
			<div class="flex items-center gap-1">
				<UIcon
					name="lucide:copyright"
					class="size-6"
				/>
				<div>2025 Reconex</div>
			</div>
			<div>
				<img
					src="https://reconex.io/wp-content/uploads/2025/01/reconex-loto-dark.svg"
					alt="Logo"
					class="w-[150px] min-w-[150px] h-auto object-contain"
				/>
			</div>
		</footer>
	</div>
</template>

<style scoped>
.artboard {
	background-image: url('https://reconex.io/wp-content/uploads/2025/02/Artboard-5.png');
	background-size: cover;
	background-position: center;
	background-repeat: no-repeat;
}
</style>
