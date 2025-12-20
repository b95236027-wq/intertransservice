<script lang="ts">
	import * as m from '$lib/paraglide/messages';

	let formData = $state({
		name: '',
		email: '',
		phone: '',
		company: '',
		message: ''
	});

	let submitted = $state(false);

	function handleSubmit(event: Event) {
		event.preventDefault();
		console.log('Form submitted:', formData);
		submitted = true;
		
		setTimeout(function() {
			submitted = false;
			formData = { name: '', email: '', phone: '', company: '', message: '' };
		}, 3000);
	}
</script>

<svelte:head>
	<title>{m.contacts_meta_title()}</title>
	<meta name="description" content={m.contacts_meta_description()} />
</svelte:head>

<!-- Page Header -->
<div class="bg-[#0f2942] py-20 relative overflow-hidden">
	<div class="absolute inset-0 pattern-overlay opacity-30"></div>
	<div class="container mx-auto px-4 relative">
		<div class="flex items-center gap-4 mb-4">
			<div class="w-16 h-[2px] bg-[#c9a227]"></div>
			<span class="text-[#c9a227] text-sm font-semibold tracking-[0.2em] uppercase">{m.contacts_page_subtitle()}</span>
		</div>
		<h1 class="text-4xl md:text-6xl font-bold text-white">{m.contacts_page_title()}</h1>
	</div>
</div>

<section class="py-20 bg-gray-100">
	<div class="container mx-auto px-4">
		<div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
			<!-- Contact Information -->
			<div>
				<h2 class="text-3xl font-bold text-[#0f2942] mb-8 section-title">{m.contacts_info_title()}</h2>
				
				<p class="text-gray-600 mb-10 leading-relaxed">
					{m.contacts_info_description()}
				</p>

				<div class="space-y-8">
					<div class="flex items-start gap-4">
						<div class="w-14 h-14 bg-[#0f2942] flex items-center justify-center flex-shrink-0">
							<svg class="w-6 h-6 text-[#c9a227]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
								<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"></path>
							</svg>
						</div>
						<div>
							<h3 class="font-bold text-[#0f2942] text-lg mb-1">{m.contacts_phone_label()}</h3>
							<a href="tel:+77019134104" class="text-gray-600 hover:text-[#c9a227] transition-colors">{m.contacts_phone()}</a>
							<p class="text-sm text-gray-500 mt-1">{m.contacts_messengers()}</p>
						</div>
					</div>

					<div class="flex items-start gap-4">
						<div class="w-14 h-14 bg-[#0f2942] flex items-center justify-center flex-shrink-0">
							<svg class="w-6 h-6 text-[#c9a227]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
								<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path>
							</svg>
						</div>
						<div>
							<h3 class="font-bold text-[#0f2942] text-lg mb-1">{m.contacts_email_label()}</h3>
							<a href="mailto:its_aktau@mail.ru" class="text-gray-600 hover:text-[#c9a227] transition-colors">{m.contacts_email()}</a>
						</div>
					</div>

					<div class="flex items-start gap-4">
						<div class="w-14 h-14 bg-[#0f2942] flex items-center justify-center flex-shrink-0">
							<svg class="w-6 h-6 text-[#c9a227]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
								<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"></path>
								<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"></path>
							</svg>
						</div>
						<div>
							<h3 class="font-bold text-[#0f2942] text-lg mb-1">{m.contacts_address_label()}</h3>
							<p class="text-gray-600">{m.contacts_address()}</p>
						</div>
					</div>

					<div class="flex items-start gap-4">
						<div class="w-14 h-14 bg-[#0f2942] flex items-center justify-center flex-shrink-0">
							<svg class="w-6 h-6 text-[#c9a227]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
								<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"></path>
							</svg>
						</div>
						<div>
							<h3 class="font-bold text-[#0f2942] text-lg mb-1">{m.contacts_hours_label()}</h3>
							<p class="text-gray-600">{m.contacts_hours_weekday()}</p>
							<p class="text-gray-600">{m.contacts_hours_saturday()}</p>
						</div>
					</div>
				</div>
			</div>

			<!-- Contact Form -->
			<div class="bg-white p-8 lg:p-10 shadow-lg">
				<h2 class="text-2xl font-bold text-[#0f2942] mb-8">{m.contacts_form_title()}</h2>
				
				{#if submitted}
					<div class="bg-green-50 border-l-4 border-green-500 text-green-700 px-4 py-3 mb-6">
						{m.contacts_form_success()}
					</div>
				{/if}

				<form onsubmit={handleSubmit} class="space-y-6">
					<div>
						<label for="name" class="block text-sm font-semibold text-[#0f2942] mb-2">{m.contacts_form_name_label()}</label>
						<input 
							type="text" 
							id="name" 
							bind:value={formData.name}
							required 
							class="w-full px-4 py-3 border border-gray-300 focus:border-[#c9a227] focus:ring-1 focus:ring-[#c9a227] outline-none transition-colors"
						/>
					</div>

					<div class="grid grid-cols-1 md:grid-cols-2 gap-6">
						<div>
							<label for="email" class="block text-sm font-semibold text-[#0f2942] mb-2">{m.contacts_form_email_label()}</label>
							<input 
								type="email" 
								id="email" 
								bind:value={formData.email}
								required 
								class="w-full px-4 py-3 border border-gray-300 focus:border-[#c9a227] focus:ring-1 focus:ring-[#c9a227] outline-none transition-colors"
							/>
						</div>

						<div>
							<label for="phone" class="block text-sm font-semibold text-[#0f2942] mb-2">{m.contacts_form_phone_label()}</label>
							<input 
								type="tel" 
								id="phone" 
								bind:value={formData.phone}
								class="w-full px-4 py-3 border border-gray-300 focus:border-[#c9a227] focus:ring-1 focus:ring-[#c9a227] outline-none transition-colors"
							/>
						</div>
					</div>

					<div>
						<label for="company" class="block text-sm font-semibold text-[#0f2942] mb-2">{m.contacts_form_company_label()}</label>
						<input 
							type="text" 
							id="company" 
							bind:value={formData.company}
							class="w-full px-4 py-3 border border-gray-300 focus:border-[#c9a227] focus:ring-1 focus:ring-[#c9a227] outline-none transition-colors"
						/>
					</div>

					<div>
						<label for="message" class="block text-sm font-semibold text-[#0f2942] mb-2">{m.contacts_form_message_label()}</label>
						<textarea 
							id="message" 
							bind:value={formData.message}
							required 
							rows="5" 
							class="w-full px-4 py-3 border border-gray-300 focus:border-[#c9a227] focus:ring-1 focus:ring-[#c9a227] outline-none transition-colors resize-none"
						></textarea>
					</div>

					<button 
						type="submit" 
						class="w-full py-4 bg-[#c9a227] text-[#0f2942] font-bold uppercase tracking-wider text-sm hover:bg-[#dbb732] transition-colors"
					>
						{m.contacts_form_submit()}
					</button>
				</form>
			</div>
		</div>
	</div>
</section>
