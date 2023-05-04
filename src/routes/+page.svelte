<script>
	import Offerings from '$lib/components/Offerings.svelte'
	import Sign from '$lib/components/Sign.svelte'
	import Showcase from '$lib/components/Showcase.svelte'
	import BlurbOne from '$lib/components/BlurbOne.svelte'
	import BlurbTwo from '$lib/components/BlurbTwo.svelte'
	import Process from '$lib/components/Process.svelte'

</script>
<div class="">
<Sign/>
<div class="space-y-14 mt-14 py-4 bg-tertiary-500">
	<Showcase />
</div>
	<div class="space-y-14 py-14 bg-secondary-800">
		<BlurbOne/>
		<Process />
	</div>
	<div class="space-y-14 py-14">
		<BlurbTwo/>
		<Offerings />
	</div>
</div>


