<script lang='ts'>
	
	// The ordering of these imports is critical to your app working properly
	import '@skeletonlabs/skeleton/themes/theme-skeleton.css';
	// If you have source.organizeImports set to true in VSCode, then it will auto change this ordering
	import '@skeletonlabs/skeleton/styles/all.css';
	// Most of your app wide CSS should be put in this file
	import '../app.postcss';
   // Your custom Skeleton theme:
	import '../theme.postcss';

	import { AppShell, AppBar } from '@skeletonlabs/skeleton';
	import Footer from '$lib/components/Footer.svelte'
</script>


<AppShell>
	<svelte:fragment slot="header">
		<AppBar gridColumns="grid-cols-3" slotDefault="place-self-center" slotTrail="place-content-end" class="px-10">

		<svelte:fragment slot="lead">
			<div class="flex flex-row space-x-3" > 
				
				<img src="logos/simple-color.svg" alt="" class="w-[32px]">	
				<div class="font-black emdash">Emdash</div> 
				
			</div>
		
		</svelte:fragment>
		<svelte:fragment slot="trail">
			<button type="button" class="btn variant-filled-tertiary px-20 border-b-4 border-tertiary-700 font-black">Contact</button>
			
		</svelte:fragment>
		</AppBar>

	</svelte:fragment>

	<svelte:fragment slot="pageHeader">
		<!-- use this if you want a sticky header -->
	</svelte:fragment>
	<!-- Router Slot -->
	<slot />
	<!-- ---- / ---- -->
	<svelte:fragment slot="pageFooter">
		<Footer/>
	</svelte:fragment>
	<svelte:fragment slot="footer">
		
	</svelte:fragment>
</AppShell>
