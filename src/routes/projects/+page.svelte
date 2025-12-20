<script lang="ts">
	import * as m from '$lib/paraglide/messages';

	interface Project {
		title: string;
		client: string;
		description: string;
		year: string;
		category: string;
	}

	const projects: Project[] = [
		{
			title: 'Major Highway Construction Equipment Supply',
			client: 'National Infrastructure Development',
			description: 'Complete logistics solution for delivering 25+ heavy construction machines including excavators, graders, and asphalt pavers for a 200km highway project.',
			year: '2024',
			category: 'Infrastructure'
		},
		{
			title: 'Mining Equipment Transportation',
			client: 'Kazakh Mining Corporation',
			description: 'International shipping and installation of large-scale mining equipment from Europe to Kazakhstan, including customs clearance and on-site commissioning.',
			year: '2023',
			category: 'Mining'
		},
		{
			title: 'Urban Development Machinery Package',
			client: 'Almaty City Development',
			description: 'Coordinated delivery of various construction machinery for multiple urban development sites, with warehousing and just-in-time delivery.',
			year: '2023',
			category: 'Urban Development'
		},
		{
			title: 'Oil & Gas Construction Support',
			client: 'Energy Sector Client',
			description: 'Specialized transportation of construction equipment to remote oil field locations, including route planning and permit management.',
			year: '2022',
			category: 'Energy'
		},
		{
			title: 'Railway Modernization Equipment',
			client: 'Kazakhstan Railways',
			description: 'Logistics management for railway construction equipment including track layers, ballast regulators, and maintenance vehicles.',
			year: '2022',
			category: 'Railway'
		},
		{
			title: 'Commercial Complex Construction',
			client: 'Private Development Group',
			description: 'Full-service package including tower cranes, concrete equipment, and material handling machinery for large commercial development.',
			year: '2021',
			category: 'Commercial'
		}
	];
</script>

<svelte:head>
	<title>Our Projects - InterTransService</title>
	<meta name="description" content="Explore successful construction machinery logistics projects completed by InterTransService across Kazakhstan and Central Asia." />
</svelte:head>

<!-- Page Header -->
<div class="bg-[#0f2942] py-20 relative overflow-hidden">
	<div class="absolute inset-0 pattern-overlay opacity-30"></div>
	<div class="container mx-auto px-4 relative">
		<div class="flex items-center gap-4 mb-4">
			<div class="w-16 h-[2px] bg-[#c9a227]"></div>
			<span class="text-[#c9a227] text-sm font-semibold tracking-[0.2em] uppercase">Portfolio</span>
		</div>
		<h1 class="text-4xl md:text-6xl font-bold text-white">Our Projects</h1>
	</div>
</div>

<!-- Introduction -->
<section class="py-16 bg-white">
	<div class="container mx-auto px-4">
		<div class="max-w-3xl">
			<p class="text-xl text-gray-600 leading-relaxed">
				Over the years, we have successfully completed numerous projects across various sectors. 
				Each project showcases our commitment to excellence, reliability, and customer satisfaction.
			</p>
		</div>
	</div>
</section>

<!-- Projects Grid -->
<section class="py-12 pb-20 bg-gray-100">
	<div class="container mx-auto px-4">
		<div class="grid grid-cols-1 md:grid-cols-2 gap-8">
			{#each projects as project}
				<div class="card-industrial bg-white p-8">
					<div class="flex items-center justify-between mb-4">
						<span class="px-4 py-1 bg-[#0f2942] text-[#c9a227] text-sm font-semibold">
							{project.category}
						</span>
						<span class="text-gray-500 text-sm font-mono">{project.year}</span>
					</div>
					
					<h3 class="text-xl font-bold text-[#0f2942] mb-2">{project.title}</h3>
					<p class="text-[#c9a227] font-medium mb-4">{project.client}</p>
					<p class="text-gray-600 leading-relaxed">{project.description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>

<!-- CTA Section -->
<section class="py-20 bg-[#0f2942] relative overflow-hidden">
	<div class="absolute inset-0 pattern-overlay opacity-30"></div>
	<div class="container mx-auto px-4 relative text-center">
		<h2 class="text-3xl md:text-4xl font-bold text-white mb-6">Have a Project in Mind?</h2>
		<p class="text-xl text-gray-300 mb-8 max-w-2xl mx-auto">
			Let's discuss how we can support your construction machinery logistics needs.
		</p>
		<a 
			href="/contacts" 
			class="inline-flex items-center gap-2 px-8 py-4 bg-[#c9a227] text-[#0f2942] font-bold uppercase tracking-wider text-sm hover:bg-[#dbb732] transition-colors"
		>
			Start a Conversation
			<svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
				<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/>
			</svg>
		</a>
	</div>
</section>
