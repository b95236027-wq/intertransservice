<script lang="ts">
	interface Position {
		title: string;
		department: string;
		location: string;
		type: string;
		description: string;
	}

	const openPositions: Position[] = [
		{
			title: 'Logistics Coordinator',
			department: 'Operations',
			location: 'Almaty, Kazakhstan',
			type: 'Full-time',
			description: 'Manage transportation schedules, coordinate with carriers, and ensure timely delivery of construction machinery.'
		},
		{
			title: 'Technical Support Engineer',
			department: 'Technical',
			location: 'Almaty, Kazakhstan',
			type: 'Full-time',
			description: 'Provide technical consultation and support for construction equipment installation and maintenance.'
		},
		{
			title: 'Sales Manager',
			department: 'Sales',
			location: 'Almaty, Kazakhstan',
			type: 'Full-time',
			description: 'Develop new business relationships and manage existing client accounts in the construction machinery sector.'
		}
	];

	let formData = $state({
		name: '',
		email: '',
		phone: '',
		position: '',
		resume: null as File | null
	});

	let submitted = $state(false);

	function handleSubmit(event: Event) {
		event.preventDefault();
		console.log('Resume submitted:', formData);
		submitted = true;
		setTimeout(function() {
			submitted = false;
			formData = { name: '', email: '', phone: '', position: '', resume: null };
		}, 3000);
	}

	function handleFileChange(event: Event) {
		const target = event.target as HTMLInputElement;
		if (target.files && target.files.length > 0) {
			formData.resume = target.files[0];
		}
	}
</script>

<svelte:head>
	<title>Careers - InterTransService</title>
	<meta name="description" content="Join the InterTransService team. Explore career opportunities in construction machinery logistics." />
</svelte:head>

<!-- Page Header -->
<div class="bg-[#0f2942] py-20 relative overflow-hidden">
	<div class="absolute inset-0 pattern-overlay opacity-30"></div>
	<div class="container mx-auto px-4 relative">
		<div class="flex items-center gap-4 mb-4">
			<div class="w-16 h-[2px] bg-[#c9a227]"></div>
			<span class="text-[#c9a227] text-sm font-semibold tracking-[0.2em] uppercase">Join Us</span>
		</div>
		<h1 class="text-4xl md:text-6xl font-bold text-white">Careers</h1>
	</div>
</div>

<!-- Why Work With Us -->
<section class="py-20 bg-white">
	<div class="container mx-auto px-4">
		<div class="mb-16">
			<span class="text-[#c9a227] text-sm font-semibold tracking-[0.2em] uppercase">Benefits</span>
			<h2 class="text-4xl font-bold text-[#0f2942] mt-2 section-title">Why Work With Us?</h2>
		</div>

		<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
			<div class="card-industrial bg-gray-50 p-8">
				<div class="w-14 h-14 bg-[#0f2942] flex items-center justify-center mb-6">
					<svg class="w-7 h-7 text-[#c9a227]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M13 7h8m0 0v8m0-8l-8 8-4-4-6 6"/>
					</svg>
				</div>
				<h3 class="text-xl font-bold text-[#0f2942] mb-3">Career Growth</h3>
				<p class="text-gray-600">Clear career paths and opportunities for advancement</p>
			</div>
			
			<div class="card-industrial bg-gray-50 p-8">
				<div class="w-14 h-14 bg-[#0f2942] flex items-center justify-center mb-6">
					<svg class="w-7 h-7 text-[#c9a227]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253"/>
					</svg>
				</div>
				<h3 class="text-xl font-bold text-[#0f2942] mb-3">Training</h3>
				<p class="text-gray-600">Continuous learning and professional development programs</p>
			</div>
			
			<div class="card-industrial bg-gray-50 p-8">
				<div class="w-14 h-14 bg-[#0f2942] flex items-center justify-center mb-6">
					<svg class="w-7 h-7 text-[#c9a227]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M3 6l3 1m0 0l-3 9a5.002 5.002 0 006.001 0M6 7l3 9M6 7l6-2m6 2l3-1m-3 1l-3 9a5.002 5.002 0 006.001 0M18 7l3 9m-3-9l-6-2m0-2v2m0 16V5m0 16H9m3 0h3"/>
					</svg>
				</div>
				<h3 class="text-xl font-bold text-[#0f2942] mb-3">Work-Life Balance</h3>
				<p class="text-gray-600">Flexible working arrangements and competitive benefits</p>
			</div>
		</div>
	</div>
</section>

<!-- Open Positions -->
{#if openPositions.length > 0}
	<section class="py-20 bg-gray-100">
		<div class="container mx-auto px-4">
			<div class="mb-16">
				<span class="text-[#c9a227] text-sm font-semibold tracking-[0.2em] uppercase">Opportunities</span>
				<h2 class="text-4xl font-bold text-[#0f2942] mt-2 section-title">Open Positions</h2>
			</div>

			<div class="space-y-4 max-w-4xl">
				{#each openPositions as position}
					<div class="card-industrial bg-white p-6">
						<div class="flex flex-wrap items-start justify-between gap-4">
							<div class="flex-grow">
								<h3 class="text-xl font-bold text-[#0f2942] mb-3">{position.title}</h3>
								<div class="flex flex-wrap gap-4 mb-4 text-sm text-gray-600">
									<span class="flex items-center gap-1">
										<svg class="w-4 h-4 text-[#c9a227]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
											<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4"/>
										</svg>
										{position.department}
									</span>
									<span class="flex items-center gap-1">
										<svg class="w-4 h-4 text-[#c9a227]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
											<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"/>
											<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"/>
										</svg>
										{position.location}
									</span>
									<span class="flex items-center gap-1">
										<svg class="w-4 h-4 text-[#c9a227]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
											<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"/>
										</svg>
										{position.type}
									</span>
								</div>
								<p class="text-gray-600">{position.description}</p>
							</div>
							<a href="#apply" class="px-6 py-3 bg-[#c9a227] text-[#0f2942] font-bold uppercase tracking-wider text-sm hover:bg-[#dbb732] transition-colors whitespace-nowrap">
								Apply Now
							</a>
						</div>
					</div>
				{/each}
			</div>
		</div>
	</section>
{/if}

<!-- Application Form -->
<section id="apply" class="py-20 bg-white">
	<div class="container mx-auto px-4">
		<div class="max-w-2xl mx-auto">
			<div class="text-center mb-12">
				<span class="text-[#c9a227] text-sm font-semibold tracking-[0.2em] uppercase">Apply</span>
				<h2 class="text-4xl font-bold text-[#0f2942] mt-2">Submit Your Resume</h2>
			</div>
			
			<div class="bg-gray-50 p-8 lg:p-10">
				{#if submitted}
					<div class="bg-green-50 border-l-4 border-green-500 text-green-700 px-4 py-3 mb-6">
						Thank you for your application! We'll review your resume and get back to you soon.
					</div>
				{/if}

				<form onsubmit={handleSubmit} class="space-y-6">
					<div>
						<label for="name" class="block text-sm font-semibold text-[#0f2942] mb-2">Full Name *</label>
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
							<label for="email" class="block text-sm font-semibold text-[#0f2942] mb-2">Email *</label>
							<input 
								type="email" 
								id="email" 
								bind:value={formData.email}
								required 
								class="w-full px-4 py-3 border border-gray-300 focus:border-[#c9a227] focus:ring-1 focus:ring-[#c9a227] outline-none transition-colors"
							/>
						</div>

						<div>
							<label for="phone" class="block text-sm font-semibold text-[#0f2942] mb-2">Phone *</label>
							<input 
								type="tel" 
								id="phone" 
								bind:value={formData.phone}
								required 
								class="w-full px-4 py-3 border border-gray-300 focus:border-[#c9a227] focus:ring-1 focus:ring-[#c9a227] outline-none transition-colors"
							/>
						</div>
					</div>

					<div>
						<label for="position" class="block text-sm font-semibold text-[#0f2942] mb-2">Position of Interest *</label>
						<select 
							id="position" 
							bind:value={formData.position}
							required 
							class="w-full px-4 py-3 border border-gray-300 focus:border-[#c9a227] focus:ring-1 focus:ring-[#c9a227] outline-none transition-colors"
						>
							<option value="">Select a position</option>
							{#each openPositions as position}
								<option value={position.title}>{position.title}</option>
							{/each}
							<option value="other">Other / General Application</option>
						</select>
					</div>

					<div>
						<label for="resume" class="block text-sm font-semibold text-[#0f2942] mb-2">Resume/CV *</label>
						<input 
							type="file" 
							id="resume" 
							onchange={handleFileChange}
							accept=".pdf,.doc,.docx"
							required 
							class="w-full px-4 py-3 border border-gray-300 focus:border-[#c9a227] focus:ring-1 focus:ring-[#c9a227] outline-none transition-colors"
						/>
						<p class="text-sm text-gray-500 mt-2">Accepted formats: PDF, DOC, DOCX (Max 5MB)</p>
					</div>

					<button 
						type="submit" 
						class="w-full py-4 bg-[#c9a227] text-[#0f2942] font-bold uppercase tracking-wider text-sm hover:bg-[#dbb732] transition-colors"
					>
						Submit Application
					</button>
				</form>
			</div>
		</div>
	</div>
</section>
