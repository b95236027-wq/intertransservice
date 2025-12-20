<script lang="ts">
	import { locales, setLocale, baseLocale, type Locale, getLocale } from '$lib/paraglide/runtime';

	const currentLocale = $derived(getLocale());

	const languageNames: Record<string, string> = {
		ru: 'РУС',
		kk: 'ҚАЗ',
		en: 'ENG'
	};

	let isOpen = $state(false);

	function toggleDropdown() {
		isOpen = !isOpen;
	}

	function closeDropdown() {
		isOpen = false;
	}

	function handleLanguageChange(locale: Locale) {
		setLocale(locale);
		closeDropdown();
	}
</script>

<div class="relative">
	<button
		onclick={toggleDropdown}
		class="flex items-center gap-2 px-3 py-2 text-gray-200 hover:text-white transition-colors rounded-md hover:bg-white/5"
		aria-label="Select language"
	>
		<svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
			<path
				stroke-linecap="round"
				stroke-linejoin="round"
				stroke-width="2"
				d="M3 5h12M9 3v2m1.048 9.5A18.022 18.022 0 016.412 9m6.088 9h7M11 21l5-10 5 10M12.751 5C11.783 10.77 8.07 15.61 3 18.129"
			></path>
		</svg>
		<span class="font-medium">{languageNames[currentLocale]}</span>
		<svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
			<path
				stroke-linecap="round"
				stroke-linejoin="round"
				stroke-width="2"
				d="M19 9l-7 7-7-7"
			></path>
		</svg>
	</button>

	{#if isOpen}
		<div
			class="absolute right-0 mt-2 w-32 bg-[#0f2942] border border-white/10 shadow-xl rounded-md overflow-hidden z-50"
		>
			{#each locales as locale}
				<button
					onclick={() => handleLanguageChange(locale)}
					class="w-full text-left px-4 py-3 text-gray-300 hover:text-white hover:bg-white/5 transition-colors {locale ===
					currentLocale
						? 'bg-white/10 font-semibold'
						: ''}"
				>
					{languageNames[locale]}
				</button>
			{/each}
		</div>
	{/if}
</div>

<svelte:window
	onclick={(e) => {
		const target = e.target as HTMLElement;
		if (!target.closest('.relative')) {
			isOpen = false;
		}
	}}
/>
