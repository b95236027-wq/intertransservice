<script lang="ts">
	import * as m from '$lib/paraglide/messages';
</script>

<section class="py-20 bg-[#0f2942] relative overflow-hidden">
	<!-- Decorative elements -->
	<div class="absolute top-0 left-0 w-64 h-64 bg-[#c9a227]/5 rounded-full -translate-x-1/2 -translate-y-1/2"></div>
	<div class="absolute bottom-0 right-0 w-96 h-96 bg-[#c9a227]/5 rounded-full translate-x-1/3 translate-y-1/3"></div>
	
	<div class="container mx-auto px-4 relative">
		<div class="max-w-4xl mx-auto">
			<!-- Section header -->
			<div class="text-center mb-12">
				<span class="text-[#c9a227] text-sm font-semibold tracking-[0.2em] uppercase">{m.home_director_subtitle()}</span>
				<h2 class="text-4xl md:text-5xl font-bold text-white mt-2">{m.home_director_title()}</h2>
			</div>

			<!-- Quote -->
			<div class="relative">
				<!-- Quote mark -->
				<div class="absolute -top-8 -left-4 text-[#c9a227]/20 quote-mark">"</div>
				
				<blockquote class="text-lg md:text-xl text-gray-300 leading-relaxed text-center italic pl-8 pr-8">
					{m.home_director_quote()}
				</blockquote>

				<!-- Quote mark end -->
				<div class="absolute -bottom-16 -right-4 text-[#c9a227]/20 quote-mark rotate-180">"</div>
			</div>

			<!-- Director info -->
			<div class="mt-16 flex flex-col items-center">
				<!-- Avatar placeholder -->
				<div class="w-20 h-20 bg-[#c9a227] rounded-full mb-4 flex items-center justify-center">
					<svg class="w-10 h-10 text-[#0f2942]" fill="currentColor" viewBox="0 0 24 24">
						<path d="M12 12c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm0 2c-2.67 0-8 1.34-8 4v2h16v-2c0-2.66-5.33-4-8-4z"/>
					</svg>
				</div>
				<div class="text-center">
					<div class="text-white font-bold text-lg">{m.home_director_name()}</div>
					<div class="text-[#c9a227] text-sm uppercase tracking-wider">{m.home_director_position()}</div>
				</div>
			</div>
		</div>
	</div>
</section>
