<script lang="ts">
	import * as m from '$lib/paraglide/messages';

	interface Advantage {
		title: string;
		description: string;
	}

	const advantages: Advantage[] = [
		{
			title: m.home_advantage1_title(),
			description: m.home_advantage1_description()
		},
		{
			title: m.home_advantage2_title(),
			description: m.home_advantage2_description()
		},
		{
			title: m.home_advantage3_title(),
			description: m.home_advantage3_description()
		},
		{
			title: m.home_advantage4_title(),
			description: m.home_advantage4_description()
		}
	];
</script>

<section class="py-20 bg-white">
	<div class="container mx-auto px-4">
		<!-- Section header -->
		<div class="mb-16">
			<span class="text-[#c9a227] text-sm font-semibold tracking-[0.2em] uppercase">{m.home_advantages_subtitle()}</span>
			<h2 class="text-4xl md:text-5xl font-bold text-[#0f2942] mt-2 section-title">{m.home_advantages_title()}</h2>
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
