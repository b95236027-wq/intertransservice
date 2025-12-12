<script lang="ts">
	interface Advantage {
		title: string;
		description: string;
	}

	const advantages: Advantage[] = [
		{
			title: 'Experienced Qualified Personnel',
			description: 'Experience and high qualifications — as a result of extensive practice for more than 10 years.'
		},
		{
			title: 'High Quality',
			description: 'All stages of work are inspected by the technical control department and quality assurance team.'
		},
		{
			title: 'Modern Equipment',
			description: 'Renewal and modernization of equipment is our way of keeping up with the times.'
		},
		{
			title: 'Certified Services',
			description: 'All our services comply with the standards of the Republic of Kazakhstan and international regulations.'
		}
	];
</script>

<section class="py-20 bg-white">
	<div class="container mx-auto px-4">
		<!-- Section header -->
		<div class="mb-16">
			<span class="text-[#c9a227] text-sm font-semibold tracking-[0.2em] uppercase">Welcome</span>
			<h2 class="text-4xl md:text-5xl font-bold text-[#0f2942] mt-2 section-title">Our Advantages</h2>
		</div>

		<!-- Advantages grid -->
		<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
			{#each advantages as advantage, index}
				<div class="card-industrial bg-gray-50 p-8 hover:bg-white hover:shadow-xl">
					<!-- Number -->
					<div class="text-6xl font-bold text-[#c9a227]/20 mb-4">
						0{index + 1}
					</div>
					
					<!-- Content -->
					<h3 class="text-xl font-bold text-[#0f2942] mb-4 leading-tight">
						{advantage.title}
					</h3>
					<p class="text-gray-600 leading-relaxed">
						{advantage.description}
					</p>
				</div>
			{/each}
		</div>
	</div>
</section>
