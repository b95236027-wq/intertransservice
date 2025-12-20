<script lang="ts">
	import * as m from '$lib/paraglide/messages';
</script>

<svelte:head>
	<title>{m.about_meta_title()}</title>
	<meta name="description" content={m.about_meta_description()} />
</svelte:head>

<!-- Page Header -->
<div class="bg-[#0f2942] py-20 relative overflow-hidden">
	<div class="absolute inset-0 pattern-overlay opacity-30"></div>
	<div class="container mx-auto px-4 relative">
		<div class="flex items-center gap-4 mb-4">
			<div class="w-16 h-[2px] bg-[#c9a227]"></div>
			<span class="text-[#c9a227] text-sm font-semibold tracking-[0.2em] uppercase">{m.about_page_subtitle()}</span>
		</div>
		<h1 class="text-4xl md:text-6xl font-bold text-white">{m.about_page_title()}</h1>
	</div>
</div>

<!-- Main Content -->
<section class="py-20 bg-white">
	<div class="container mx-auto px-4">
		<div class="max-w-4xl">
			<h2 class="text-3xl font-bold text-[#0f2942] mb-8 section-title">{m.about_story_title()}</h2>
			
			<div class="prose prose-lg text-gray-600 space-y-6">
				<p>{m.about_story_p1()}</p>
				<p>{m.about_story_p2()}</p>
				<p>{m.about_story_p3()}</p>
			</div>
		</div>
	</div>
</section>

<!-- Values Section -->
<section class="py-20 bg-gray-100">
	<div class="container mx-auto px-4">
		<div class="mb-16">
			<span class="text-[#c9a227] text-sm font-semibold tracking-[0.2em] uppercase">{m.about_values_subtitle()}</span>
			<h2 class="text-4xl font-bold text-[#0f2942] mt-2 section-title">{m.about_values_title()}</h2>
		</div>
		
		<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
			<div class="card-industrial bg-white p-8">
				<div class="w-14 h-14 bg-[#0f2942] flex items-center justify-center mb-6">
					<svg class="w-7 h-7 text-[#c9a227]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M9 12l2 2 4-4M7.835 4.697a3.42 3.42 0 001.946-.806 3.42 3.42 0 014.438 0 3.42 3.42 0 001.946.806 3.42 3.42 0 013.138 3.138 3.42 3.42 0 00.806 1.946 3.42 3.42 0 010 4.438 3.42 3.42 0 00-.806 1.946 3.42 3.42 0 01-3.138 3.138 3.42 3.42 0 00-1.946.806 3.42 3.42 0 01-4.438 0 3.42 3.42 0 00-1.946-.806 3.42 3.42 0 01-3.138-3.138 3.42 3.42 0 00-.806-1.946 3.42 3.42 0 010-4.438 3.42 3.42 0 00.806-1.946 3.42 3.42 0 013.138-3.138z"/>
					</svg>
				</div>
				<h3 class="text-xl font-bold text-[#0f2942] mb-4">{m.about_value1_title()}</h3>
				<p class="text-gray-600">{m.about_value1_description()}</p>
			</div>
			
			<div class="card-industrial bg-white p-8">
				<div class="w-14 h-14 bg-[#0f2942] flex items-center justify-center mb-6">
					<svg class="w-7 h-7 text-[#c9a227]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z"/>
					</svg>
				</div>
				<h3 class="text-xl font-bold text-[#0f2942] mb-4">{m.about_value2_title()}</h3>
				<p class="text-gray-600">{m.about_value2_description()}</p>
			</div>
			
			<div class="card-industrial bg-white p-8">
				<div class="w-14 h-14 bg-[#0f2942] flex items-center justify-center mb-6">
					<svg class="w-7 h-7 text-[#c9a227]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M13 10V3L4 14h7v7l9-11h-7z"/>
					</svg>
				</div>
				<h3 class="text-xl font-bold text-[#0f2942] mb-4">{m.about_value3_title()}</h3>
				<p class="text-gray-600">{m.about_value3_description()}</p>
			</div>
		</div>
	</div>
</section>

<!-- CTA Section -->
<section class="py-20 bg-[#0f2942] relative overflow-hidden">
	<div class="absolute inset-0 pattern-overlay opacity-30"></div>
	<div class="container mx-auto px-4 relative text-center">
		<h2 class="text-3xl md:text-4xl font-bold text-white mb-6">{m.about_cta_title()}</h2>
		<p class="text-xl text-gray-300 mb-8 max-w-2xl mx-auto">
			{m.about_cta_description()}
		</p>
		<a 
			href="/contacts" 
			class="inline-flex items-center gap-2 px-8 py-4 bg-[#c9a227] text-[#0f2942] font-bold uppercase tracking-wider text-sm hover:bg-[#dbb732] transition-colors"
		>
			{m.about_cta_button()}
			<svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
				<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/>
			</svg>
		</a>
	</div>
</section>
