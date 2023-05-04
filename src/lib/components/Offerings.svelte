<script lang="ts">
	let rate = 4993;
	function calcRate(rate: number, discount: number) {
		return rate - rate * discount;
	}
	function calcSavings(rate: number, discount: number) {
		return rate * discount;
	}
    
    function handleAnchorClick (event) {
		event.preventDefault()
		const link = event.currentTarget
        const anchor = document.querySelector(link.hash)
		window.scrollTo({
			top: anchor?.offsetTop,
			behavior: 'smooth'
		})
	}

	let offerings = [
		{
			title: 'Monthly',
			link: '/',
			description: 'Our most flexible plan; pay as you go & cancel at any time.',
			cta: 'Subscribe',
			cta_btn_color: 'variant-filled-success',
			cta_btn_border: 'border-success-700',
			rate: calcRate(rate, 0),
			savings: calcSavings(rate, 0),
			highlight: false
		},
		{
			title: 'Quarterly',
			link: '/',
			description: '<b>Save 10%</b>. Great for large projects (~3-6 sprints).',
			cta: 'Subscribe',
			cta_btn_color: 'variant-filled-primary',
			cta_btn_border: 'border-primary-700',
			rate: calcRate(rate, 0.1),
			savings: calcSavings(rate, 0.1),
			highlight: false
		},
		{
			title: 'Yearly',
			link: '/',
			description:
				'<b>Save 20%.</b> Supercharge your design output at a third of the cost of a full-time designer.',
			cta: 'Subscribe',
			cta_btn_color: 'variant-filled-tertiary',
			cta_btn_border: 'border-tertiary-700',
			rate: calcRate(rate, 0.2),
			savings: calcSavings(rate, 0.2),
			highlight: false
		},
		{
			title: 'Book a Call',
			link: '/',
			description: 'Learn more about how Emdash works and how we can help you.',
			cta: 'Contact',
			cta_btn_color: 'variant-ghost-surface',
			cta_btn_border: 'border-surface-500',
			highlight: true
		}
	];
</script>

<div id="meow" class="flex flex-col lg:flex-row py-7">
	{#each offerings as { title, link, description, cta, cta_btn_color, cta_btn_border, rate, highlight }}
		<a
			class="card card-hover flex flex-col space-y-4 py-4 {highlight
				? 'variant-ringed-success'
				: 'variant-ghost-surface'} m-2 lg:w-3/12"
			href={link}
            on:click={handleAnchorClick}
		>
			<div class="card-header flex justify-center p-4">
				<div class="text-3xl emdash">{title}</div>
			</div>
			<div class="card-body p-4">
				<div class="text-lg text-center">{@html description}</div>
			</div>
			<div class="card-footer flex flex-col flex-grow justify-end p-4 space-y-8">
				<div class="flex flex-row justify-center items-end space-x-1">
					{#if rate}
						<div class="text-4xl font-black mt-4">
							${rate}
						</div>
						<div>/m</div>
					{/if}
				</div>
				<button
					type="button"
					class="btn border-b-4 {cta_btn_color} {cta_btn_border} rounded-none font-black"
				>
					{@html cta}</button
				>
			</div>
		</a>
	{/each}
</div>
