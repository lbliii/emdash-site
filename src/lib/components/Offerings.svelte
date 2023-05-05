<script lang="ts">
	let rate = 4993;
	function calcRate(rate: number, discount: number) {
		return rate - rate * discount;
	}
	function calcSavings(rate: number, discount: number) {
		return rate * discount;
	}
    

	let offerings = [
		{
			title: 'Monthly',
			link: 'https://buy.stripe.com/00gbJG3UDdMAbVSeUU',
			description: '<b>Our most flexible plan.</b> <br> Pay as you go & cancel at any time.',
			cta: 'Subscribe',
			cta_btn_color: 'variant-filled-success',
			cta_btn_border: 'border-success-700',
			rate: calcRate(rate, 0),
			savings: calcSavings(rate, 0),
			highlight: false
		},
		{
			title: 'Quarterly',
			link: 'https://buy.stripe.com/cN2bJGaj1cIw7FCfYZ',
			description: '<b>Save 10%</b>. <br> Great for larger projects like multi-page web designs (~3-6 sprints).',
			cta: 'Subscribe',
			cta_btn_color: 'variant-filled-primary',
			cta_btn_border: 'border-primary-700',
			rate: calcRate(rate, 0.1),
			savings: calcSavings(rate, 0.1),
			highlight: false
		},
		{
			title: 'Yearly',
			link: 'https://buy.stripe.com/28obJG0IrcIw2lieUW',
			description:
				'<b>Save 20%.</b> <br> Supercharge your design output at 1/3 the cost of a full-time designer.',
			cta: 'Subscribe',
			cta_btn_color: 'variant-filled-tertiary',
			cta_btn_border: 'border-tertiary-700',
			rate: calcRate(rate, 0.2),
			savings: calcSavings(rate, 0.2),
			highlight: false
		},
		{
			title: 'Book a Call',
			link: 'https://calendly.com/emdashbook',
			description: '<b>Have questions?</b> <br> Book a call with us to learn more.',
			cta: 'Contact',
			cta_btn_color: 'variant-ghost-tertiary',
			cta_btn_border: 'border-tertiary-500',
			highlight: true
		}
	];
</script>

<div id="meow" class="flex flex-col lg:flex-row pt-7">
	{#each offerings as { title, link, description, cta, cta_btn_color, cta_btn_border, rate, highlight }}
		<a
			class="card card-hover flex flex-col space-y-4 py-4 {highlight
				? 'variant-ringed-success'
				: 'variant-ghost-surface'} m-2 lg:w-3/12"
			href="{link}"
		>
			<div class="card-header flex justify-center p-4">
				<div class="text-3xl emdash">{title}</div>
			</div>
			<div class="card-body p-4">
				<div class="text-xl text-center font-thin">{@html description}</div>
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

				{#if !highlight}
				<button
					type="button"
					class="btn border-b-4 {cta_btn_color} {cta_btn_border} {highlight? '' : 'rounded-none'} font-black"
				>
					{@html cta}</button
				>
				{:else}
				<button type="button" class="emdash text-md text-center hover:text-primary-500 pb-3">
					▶︎ Contact
				</button>
				
				{/if }
				
			</div>
		</a>
	{/each}
</div>

<div class="flex flex-row justify-center space-x-8 font-thin text-lg">
	<div>
		⭐ Unlimited requests 
	</div>
	<div>
		⭐ Unlimited revisions 
	</div>
	<div>
		⭐ Cancel at any time 
	</div>
</div>
