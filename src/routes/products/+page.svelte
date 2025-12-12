<script lang="ts">
	interface Service {
		title: string;
		description: string;
		features: string[];
	}

	const services: Service[] = [
		{
			title: 'Heavy Machinery Transport',
			description: 'Specialized transportation services for all types of construction equipment',
			features: [
				'Excavators and bulldozers',
				'Tower cranes and mobile cranes',
				'Concrete pumps and mixers',
				'Road construction equipment'
			]
		},
		{
			title: 'International Shipping',
			description: 'Cross-border logistics with full documentation support',
			features: [
				'Customs clearance assistance',
				'International documentation',
				'Multi-modal transportation',
				'Real-time tracking'
			]
		},
		{
			title: 'Equipment Installation',
			description: 'Professional on-site installation and setup services',
			features: [
				'Technical commissioning',
				'Safety inspection',
				'Operator training',
				'Performance testing'
			]
		},
		{
			title: 'Warehousing Solutions',
			description: 'Secure storage facilities for equipment and parts',
			features: [
				'Climate-controlled storage',
				'24/7 security monitoring',
				'Inventory management',
				'Short and long-term options'
			]
		},
		{
			title: 'Parts Supply',
			description: 'Comprehensive spare parts sourcing and delivery',
			features: [
				'Original manufacturer parts',
				'Fast delivery worldwide',
				'Parts warranty',
				'Technical consultation'
			]
		},
		{
			title: 'Technical Support',
			description: 'Expert consultation throughout equipment lifecycle',
			features: [
				'Equipment selection advice',
				'Maintenance planning',
				'Technical troubleshooting',
				'Upgrade recommendations'
			]
		}
	];
</script>

<svelte:head>
	<title>Our Services - InterTransService</title>
	<meta name="description" content="Comprehensive construction machinery logistics services including transport, installation, warehousing, and technical support." />
</svelte:head>

<!-- Page Header -->
<div class="bg-[#0f2942] py-20 relative overflow-hidden">
	<div class="absolute inset-0 pattern-overlay opacity-30"></div>
	<div class="container mx-auto px-4 relative">
		<div class="flex items-center gap-4 mb-4">
			<div class="w-16 h-[2px] bg-[#c9a227]"></div>
			<span class="text-[#c9a227] text-sm font-semibold tracking-[0.2em] uppercase">What We Offer</span>
		</div>
		<h1 class="text-4xl md:text-6xl font-bold text-white">Our Services</h1>
	</div>
</div>

<!-- Services Grid -->
<section class="py-20 bg-gray-100">
	<div class="container mx-auto px-4">
		<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
			{#each services as service, index}
				<div class="card-industrial bg-white p-8 h-full">
					<!-- Number -->
					<div class="text-5xl font-bold text-[#c9a227]/20 mb-4">0{index + 1}</div>
					
					<h2 class="text-2xl font-bold text-[#0f2942] mb-4">{service.title}</h2>
					<p class="text-gray-600 mb-6">{service.description}</p>
					
					<ul class="space-y-3">
						{#each service.features as feature}
							<li class="flex items-start gap-3">
								<svg class="w-5 h-5 text-[#c9a227] mt-0.5 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
									<path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"></path>
								</svg>
								<span class="text-gray-700">{feature}</span>
							</li>
						{/each}
					</ul>
				</div>
			{/each}
		</div>
	</div>
</section>

<!-- CTA Section -->
<section class="py-20 bg-[#0f2942] relative overflow-hidden">
	<div class="absolute inset-0 pattern-overlay opacity-30"></div>
	<div class="container mx-auto px-4 relative text-center">
		<h2 class="text-3xl md:text-4xl font-bold text-white mb-6">Need a Custom Solution?</h2>
		<p class="text-xl text-gray-300 mb-8 max-w-2xl mx-auto">
			We understand that every project is unique. Let us create a tailored logistics solution for your needs.
		</p>
		<a 
			href="/contacts" 
			class="inline-flex items-center gap-2 px-8 py-4 bg-[#c9a227] text-[#0f2942] font-bold uppercase tracking-wider text-sm hover:bg-[#dbb732] transition-colors"
		>
			Contact Us
			<svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
				<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/>
			</svg>
		</a>
	</div>
</section>
