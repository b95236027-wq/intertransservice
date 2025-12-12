<script lang="ts">
	import LeadershipTeam from '$lib/components/LeadershipTeam.svelte';
</script>

<svelte:head>
	<title>Our Team - InterTransService</title>
	<meta name="description" content="Meet the leadership team at InterTransService, experienced professionals dedicated to excellence in construction machinery logistics." />
</svelte:head>

<!-- Page Header -->
<div class="bg-[#0f2942] py-20 relative overflow-hidden">
	<div class="absolute inset-0 pattern-overlay opacity-30"></div>
	<div class="container mx-auto px-4 relative">
		<div class="flex items-center gap-4 mb-4">
			<div class="w-16 h-[2px] bg-[#c9a227]"></div>
			<span class="text-[#c9a227] text-sm font-semibold tracking-[0.2em] uppercase">Our People</span>
		</div>
		<h1 class="text-4xl md:text-6xl font-bold text-white">Our Team</h1>
	</div>
</div>

<!-- Introduction -->
<section class="py-16 bg-white">
	<div class="container mx-auto px-4">
		<div class="max-w-3xl">
			<p class="text-xl text-gray-600 leading-relaxed">
				Our team is comprised of experienced professionals who are passionate about 
				delivering exceptional service. With expertise spanning logistics, engineering, 
				and customer service, we work together to ensure your success.
			</p>
		</div>
	</div>
</section>

<LeadershipTeam />

<!-- CTA Section -->
<section class="py-20 bg-[#0f2942] relative overflow-hidden">
	<div class="absolute inset-0 pattern-overlay opacity-30"></div>
	<div class="container mx-auto px-4 relative text-center">
		<h2 class="text-3xl md:text-4xl font-bold text-white mb-6">Join Our Team</h2>
		<p class="text-xl text-gray-300 mb-8 max-w-2xl mx-auto">
			We're always looking for talented individuals to join our growing team.
		</p>
		<a 
			href="/careers" 
			class="inline-flex items-center gap-2 px-8 py-4 bg-[#c9a227] text-[#0f2942] font-bold uppercase tracking-wider text-sm hover:bg-[#dbb732] transition-colors"
		>
			View Open Positions
			<svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
				<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/>
			</svg>
		</a>
	</div>
</section>
