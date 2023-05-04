<script>
	import Offerings from '$lib/components/Offerings.svelte'
	import Sign from '$lib/components/Sign.svelte'
	import Showcase from '$lib/components/Showcase.svelte'
</script>

<div class="container h-full mx-auto flex justify-center items-center">
	<div class="space-y-10">
		<Sign/>
		<Showcase />
		<Offerings />
	</div>
</div>
