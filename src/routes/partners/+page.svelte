<script lang="ts">
	import * as m from '$lib/paraglide/messages';
</script>

<svelte:head>
	<title>{m.partners_meta_title()}</title>
	<meta name="description" content={m.partners_meta_description()} />
</svelte:head>

<!-- Page Header -->
<div class="bg-[#0f2942] py-20 relative overflow-hidden">
	<div class="absolute inset-0 pattern-overlay opacity-30"></div>
	<div class="container mx-auto px-4 relative">
		<div class="flex items-center gap-4 mb-4">
			<div class="w-16 h-[2px] bg-[#c9a227]"></div>
			<span class="text-[#c9a227] text-sm font-semibold tracking-[0.2em] uppercase">{m.partners_page_subtitle()}</span>
		</div>
		<h1 class="text-4xl md:text-6xl font-bold text-white">{m.partners_page_title()}</h1>
	</div>
</div>

<!-- Introduction -->
<section class="py-20 bg-white">
	<div class="container mx-auto px-4">
		<div class="max-w-4xl mx-auto text-center">
			<h2 class="text-3xl font-bold text-[#0f2942] mb-6">{m.partners_intro_title()}</h2>
			<p class="text-xl text-gray-600 leading-relaxed">
				{m.partners_intro_description()}
			</p>
		</div>
	</div>
</section>

<!-- Partners Grid -->
<section class="py-12 bg-gray-100">
	<div class="container mx-auto px-4">
		<div class="grid grid-cols-2 md:grid-cols-4 gap-6">
			{#each Array(8) as _, i}
				<div class="card-industrial bg-white p-8 aspect-square flex items-center justify-center">
					<div class="text-center">
						<div class="w-16 h-16 bg-gray-200 mx-auto mb-4 flex items-center justify-center">
							<svg class="w-8 h-8 text-gray-400" fill="currentColor" viewBox="0 0 24 24">
								<path d="M12 7V3H2v18h20V7H12zM6 19H4v-2h2v2zm0-4H4v-2h2v2zm0-4H4V9h2v2zm0-4H4V5h2v2zm4 12H8v-2h2v2zm0-4H8v-2h2v2zm0-4H8V9h2v2zm0-4H8V5h2v2zm10 12h-8v-2h2v-2h-2v-2h2v-2h-2V9h8v10zm-2-8h-2v2h2v-2zm0 4h-2v2h2v-2z"/>
							</svg>
						</div>
						<p class="text-sm text-gray-500 font-medium">Partner {i + 1}</p>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<!-- Partner Categories -->
<section class="py-20 bg-white">
	<div class="container mx-auto px-4">
		<div class="mb-16 text-center">
			<span class="text-[#c9a227] text-sm font-semibold tracking-[0.2em] uppercase">{m.partners_categories_subtitle()}</span>
			<h2 class="text-4xl font-bold text-[#0f2942] mt-2">{m.partners_categories_title()}</h2>
		</div>
		
		<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
			<div class="text-center">
				<div class="w-20 h-20 bg-[#0f2942] mx-auto mb-6 flex items-center justify-center">
					<svg class="w-10 h-10 text-[#c9a227]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4"/>
					</svg>
				</div>
				<h3 class="text-xl font-bold text-[#0f2942] mb-3">{m.partners_category1_title()}</h3>
				<p class="text-gray-600">{m.partners_category1_description()}</p>
			</div>
			
			<div class="text-center">
				<div class="w-20 h-20 bg-[#0f2942] mx-auto mb-6 flex items-center justify-center">
					<svg class="w-10 h-10 text-[#c9a227]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M8 7h12m0 0l-4-4m4 4l-4 4m0 6H4m0 0l4 4m-4-4l4-4"/>
					</svg>
				</div>
				<h3 class="text-xl font-bold text-[#0f2942] mb-3">{m.partners_category2_title()}</h3>
				<p class="text-gray-600">{m.partners_category2_description()}</p>
			</div>
			
			<div class="text-center">
				<div class="w-20 h-20 bg-[#0f2942] mx-auto mb-6 flex items-center justify-center">
					<svg class="w-10 h-10 text-[#c9a227]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.296.07 2.572-1.065z"/>
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"/>
					</svg>
				</div>
				<h3 class="text-xl font-bold text-[#0f2942] mb-3">{m.partners_category3_title()}</h3>
				<p class="text-gray-600">{m.partners_category3_description()}</p>
			</div>
		</div>
	</div>
</section>

<!-- CTA Section -->
<section class="py-20 bg-[#0f2942] relative overflow-hidden">
	<div class="absolute inset-0 pattern-overlay opacity-30"></div>
	<div class="container mx-auto px-4 relative text-center">
		<h2 class="text-3xl md:text-4xl font-bold text-white mb-6">{m.partners_cta_title()}</h2>
		<p class="text-xl text-gray-300 mb-8 max-w-2xl mx-auto">
			{m.partners_cta_description()}
		</p>
		<a 
			href="/contacts" 
			class="inline-flex items-center gap-2 px-8 py-4 bg-[#c9a227] text-[#0f2942] font-bold uppercase tracking-wider text-sm hover:bg-[#dbb732] transition-colors"
		>
			{m.partners_cta_button()}
			<svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
				<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/>
			</svg>
		</a>
	</div>
</section>
