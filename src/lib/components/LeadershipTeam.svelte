<script lang="ts">
	interface Leader {
		name: string;
		position: string;
	}

	const leaders: Leader[] = [
		{
			name: 'Director Name',
			position: 'Director'
		},
		{
			name: 'Chief Engineer Name',
			position: 'Chief Engineer'
		},
		{
			name: 'Operations Manager',
			position: 'Head of Operations'
		},
		{
			name: 'Logistics Director',
			position: 'Deputy Director'
		}
	];
</script>

<section class="py-20 bg-white">
	<div class="container mx-auto px-4">
		<!-- Section header -->
		<div class="mb-16 text-center">
			<span class="text-[#c9a227] text-sm font-semibold tracking-[0.2em] uppercase">Our People</span>
			<h2 class="text-4xl md:text-5xl font-bold text-[#0f2942] mt-2 section-title section-title-center">Leadership</h2>
		</div>

		<!-- Team grid -->
		<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8">
			{#each leaders as leader}
				<div class="group text-center">
					<!-- Photo placeholder -->
					<div class="relative mb-6 overflow-hidden">
						<div class="aspect-[3/4] bg-gray-200 flex items-center justify-center">
							<svg class="w-24 h-24 text-gray-400" fill="currentColor" viewBox="0 0 24 24">
								<path d="M12 12c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm0 2c-2.67 0-8 1.34-8 4v2h16v-2c0-2.66-5.33-4-8-4z"/>
							</svg>
						</div>
						<!-- Overlay on hover -->
						<div class="absolute inset-0 bg-[#0f2942]/80 opacity-0 group-hover:opacity-100 transition-opacity flex items-center justify-center">
							<div class="w-12 h-12 border-2 border-[#c9a227] rounded-full flex items-center justify-center">
								<svg class="w-6 h-6 text-[#c9a227]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
									<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 16h-1v-4h-1m1-4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"/>
								</svg>
							</div>
						</div>
					</div>
					
					<!-- Info -->
					<h3 class="text-lg font-bold text-[#0f2942] mb-1">{leader.name}</h3>
					<p class="text-[#c9a227] text-sm uppercase tracking-wider">{leader.position}</p>
				</div>
			{/each}
		</div>
	</div>
</section>
