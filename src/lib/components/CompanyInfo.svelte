<script lang="ts">
	import * as m from '$lib/paraglide/messages';
</script>

<section class="py-20 bg-[#0f2942] relative overflow-hidden">
	<!-- Decorative pattern -->
	<div class="absolute inset-0 pattern-overlay opacity-50"></div>
	
	<div class="container mx-auto px-4 relative">
		<div class="max-w-4xl mx-auto text-center">
			<!-- Company name -->
			<div class="flex items-center justify-center gap-4 mb-6">
				<div class="w-16 h-16 bg-[#c9a227] rounded flex items-center justify-center">
					<span class="text-[#0f2942] font-bold text-2xl">ITS</span>
				</div>
			</div>
			
			<h2 class="text-3xl md:text-4xl font-bold text-white mb-6">
				{m.home_company_title()}
			</h2>
			
			<p class="text-xl md:text-2xl text-gray-300 leading-relaxed font-light">
				{m.home_company_description()} 
				<span class="text-[#c9a227]">{m.home_company_highlight()}</span> 
				{m.home_company_suffix()}
			</p>
		</div>
	</div>
</section>

