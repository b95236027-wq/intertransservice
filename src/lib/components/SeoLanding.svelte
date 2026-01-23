<script lang="ts">
	export let title: string;
	export let description: string;
	export let h1: string;
	export let eyebrow: string = 'АРЕНДА ТЕХНИКИ';
	export let lead: string;
	export let bullets: string[] = [];
	export let faq: { q: string; a: string }[] = [];
	export let related: { href: string; label: string }[] = [];

	const canonical = `https://intertransservice.kz${typeof window !== 'undefined' ? window.location.pathname : ''}`;
</script>

<svelte:head>
	<title>{title} | InterTransService</title>
	<meta name="description" content={description} />
	<link rel="canonical" href={canonical} />
	<meta property="og:title" content={title} />
	<meta property="og:description" content={description} />
	<meta property="og:type" content="website" />
	<meta property="og:url" content={canonical} />
</svelte:head>

<!-- Hero -->
<div class="bg-[#0f2942] py-20 relative overflow-hidden">
	<div class="absolute inset-0 pattern-overlay opacity-30"></div>
	<div class="container mx-auto px-4 relative">
		<div class="flex items-center gap-4 mb-4">
			<div class="w-16 h-[2px] bg-[#c9a227]"></div>
			<span class="text-[#c9a227] text-sm font-semibold tracking-[0.2em] uppercase">{eyebrow}</span>
		</div>
		<h1 class="text-4xl md:text-6xl font-bold text-white">{h1}</h1>
		<p class="text-xl text-gray-300 mt-4 max-w-3xl">{lead}</p>
		<div class="mt-8 flex flex-col sm:flex-row gap-4">
			<a href="/contacts" class="inline-flex items-center justify-center gap-2 px-8 py-4 bg-[#c9a227] text-[#0f2942] font-bold uppercase tracking-wider text-sm hover:bg-[#dbb732] transition-colors">
				Заказать
				<svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
					<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/>
				</svg>
			</a>
			<a href="tel:+77019134104" class="inline-flex items-center justify-center gap-2 px-8 py-4 border border-white/30 text-white font-bold uppercase tracking-wider text-sm hover:bg-white/10 transition-colors">
				Позвонить
			</a>
		</div>
	</div>
</div>

<!-- Content -->
<section class="py-16 bg-gray-100">
	<div class="container mx-auto px-4">
		<div class="grid grid-cols-1 lg:grid-cols-3 gap-10">
			<div class="lg:col-span-2">
				<div class="card-industrial bg-white p-8">
					<h2 class="text-2xl font-bold text-[#0f2942] mb-4">Условия аренды</h2>
					<p class="text-gray-700 leading-relaxed mb-6">
						Работаем с промышленными и строительными объектами. Подача техники по согласованию, опытный экипаж,
						полный пакет документов. Если нужна консультация по подбору тоннажа — поможем.
					</p>
					{#if bullets.length}
						<ul class="space-y-2">
							{#each bullets as b}
								<li class="flex items-start gap-2 text-gray-700">
									<svg class="w-5 h-5 text-[#c9a227] mt-0.5 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
										<path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"></path>
									</svg>
									<span>{b}</span>
								</li>
							{/each}
						</ul>
					{/if}
				</div>

				{#if faq.length}
					<div class="card-industrial bg-white p-8 mt-8">
						<h2 class="text-2xl font-bold text-[#0f2942] mb-6">Частые вопросы</h2>
						<div class="space-y-4">
							{#each faq as item}
								<div class="border border-gray-200 rounded-lg p-4">
									<div class="font-semibold text-[#0f2942]">{item.q}</div>
									<div class="text-gray-700 mt-2 leading-relaxed">{item.a}</div>
								</div>
							{/each}
						</div>
					</div>
				{/if}
			</div>

			<!-- Sidebar -->
			<div class="lg:col-span-1">
				<div class="card-industrial bg-white p-8 sticky top-24">
					<h3 class="text-xl font-bold text-[#0f2942] mb-4">Быстрые ссылки</h3>
					<div class="space-y-2">
						{#each related as r}
							<a href={r.href} class="block px-4 py-3 rounded-lg bg-gray-50 hover:bg-gray-100 text-[#0f2942] font-semibold">
								{r.label}
							</a>
						{/each}
					</div>
					<div class="mt-6 pt-6 border-t border-gray-200">
						<div class="text-sm text-gray-600 mb-2">Связаться</div>
						<a href="tel:+77019134104" class="block font-bold text-[#0f2942] text-lg">+7 (701) 913-41-04</a>
						<a href="mailto:its_aktau@mail.ru" class="block text-gray-700 mt-1">its_aktau@mail.ru</a>
						<a href="/contacts" class="mt-4 inline-flex items-center gap-2 text-[#c9a227] font-semibold">
							Открыть контакты
							<svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
								<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"></path>
							</svg>
						</a>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>
