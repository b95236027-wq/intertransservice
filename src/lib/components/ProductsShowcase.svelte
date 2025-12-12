<script lang="ts">
	interface Product {
		title: string;
		description: string;
	}

	const products: Product[] = [
		{
			title: 'Heavy Machinery Transport',
			description: 'Specialized transportation services for excavators, bulldozers, cranes, and other heavy construction equipment.'
		},
		{
			title: 'International Shipping',
			description: 'Cross-border logistics solutions with customs clearance and documentation handling.'
		},
		{
			title: 'Equipment Installation',
			description: 'Professional on-site installation and commissioning services for construction machinery.'
		},
		{
			title: 'Warehousing Solutions',
			description: 'Secure storage facilities designed for construction equipment and spare parts.'
		},
		{
			title: 'Parts & Components',
			description: 'Comprehensive spare parts sourcing and delivery for all major machinery brands.'
		},
		{
			title: 'Technical Consultation',
			description: 'Expert consultation and technical support throughout the equipment lifecycle.'
		}
	];
</script>

<section class="py-20 bg-gray-100">
	<div class="container mx-auto px-4">
		<!-- Section header -->
		<div class="mb-16">
			<span class="text-[#c9a227] text-sm font-semibold tracking-[0.2em] uppercase">What We Offer</span>
			<h2 class="text-4xl md:text-5xl font-bold text-[#0f2942] mt-2 section-title">Our Services</h2>
		</div>

		<!-- Products grid -->
		<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
			{#each products as product, index}
				<a href="/products" class="group">
					<div class="card-industrial bg-white p-8 h-full">
						<!-- Icon placeholder with number -->
						<div class="flex items-center justify-between mb-6">
							<div class="w-14 h-14 bg-[#0f2942] flex items-center justify-center">
								<svg class="w-7 h-7 text-[#c9a227]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
									{#if index === 0}
										<path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M8 7h12m0 0l-4-4m4 4l-4 4m0 6H4m0 0l4 4m-4-4l4-4"/>
									{:else if index === 1}
										<path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M3.055 11H5a2 2 0 012 2v1a2 2 0 002 2 2 2 0 012 2v2.945M8 3.935V5.5A2.5 2.5 0 0010.5 8h.5a2 2 0 012 2 2 2 0 104 0 2 2 0 012-2h1.064M15 20.488V18a2 2 0 012-2h3.064M21 12a9 9 0 11-18 0 9 9 0 0118 0z"/>
									{:else if index === 2}
										<path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.296.07 2.572-1.065z"/>
										<path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"/>
									{:else if index === 3}
										<path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M19 11H5m14 0a2 2 0 012 2v6a2 2 0 01-2 2H5a2 2 0 01-2-2v-6a2 2 0 012-2m14 0V9a2 2 0 00-2-2M5 11V9a2 2 0 012-2m0 0V5a2 2 0 012-2h6a2 2 0 012 2v2M7 7h10"/>
									{:else if index === 4}
										<path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M4 7v10c0 2.21 3.582 4 8 4s8-1.79 8-4V7M4 7c0 2.21 3.582 4 8 4s8-1.79 8-4M4 7c0-2.21 3.582-4 8-4s8 1.79 8 4"/>
									{:else}
										<path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M18.364 5.636l-3.536 3.536m0 5.656l3.536 3.536M9.172 9.172L5.636 5.636m3.536 9.192l-3.536 3.536M21 12a9 9 0 11-18 0 9 9 0 0118 0zm-5 0a4 4 0 11-8 0 4 4 0 018 0z"/>
									{/if}
								</svg>
							</div>
							<svg class="w-5 h-5 text-gray-400 group-hover:text-[#c9a227] group-hover:translate-x-1 transition-all" fill="none" stroke="currentColor" viewBox="0 0 24 24">
								<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/>
							</svg>
						</div>
						
						<!-- Content -->
						<h3 class="text-xl font-bold text-[#0f2942] mb-3 group-hover:text-[#c9a227] transition-colors">
							{product.title}
						</h3>
						<p class="text-gray-600 leading-relaxed">
							{product.description}
						</p>
					</div>
				</a>
			{/each}
		</div>

		<!-- View all link -->
		<div class="mt-12 text-center">
			<a 
				href="/products" 
				class="inline-flex items-center gap-2 px-8 py-4 bg-[#0f2942] text-white font-bold uppercase tracking-wider text-sm hover:bg-[#1a365d] transition-colors"
			>
				View All Services
				<svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
					<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/>
				</svg>
			</a>
		</div>
	</div>
</section>
