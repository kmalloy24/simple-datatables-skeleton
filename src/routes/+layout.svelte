<script lang="ts">
	import '../app.postcss';
	import { AppShell, AppBar } from '@skeletonlabs/skeleton';

	// Floating UI for Popups
	import { computePosition, autoUpdate, flip, shift, offset, arrow } from '@floating-ui/dom';
	import { storePopup } from '@skeletonlabs/skeleton';
	storePopup.set({ computePosition, autoUpdate, flip, shift, offset, arrow });
</script>

<!-- App Shell -->
<AppShell>
	<svelte:fragment slot="header">
		<!-- App Bar -->
		<AppBar gridColumns="grid-cols-3" slotDefault="place-self-center" slotTrail="place-content-end">
			<!-- Logo -->
			<svelte:fragment slot="lead">
				<span class="flex">
					<a class="anchor" href="/">
						<img src="/logo.png" class="w-10 ml-2" alt="home" />
					</a>
				</span></svelte:fragment
			>

			<!-- Github  -->
			<svelte:fragment slot="trail">
				<a href="https://github.com/kmalloy24/simple-datatables-skeleton" target="_blank">
					<img class="h-8 mr-2" src="/github.png" alt="github" />
				</a>
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>
	<!-- Banner -->
	<div class="variant-filled-primary p-4">
		<div class="mx-auto w-full max-w-7xl text-center">
			<p>
				This project has been <strong>depreciated.</strong> Please refer to the official integration
				guide in the
				<a
					class="text-tertiary-500 underline"
					href="https://www.skeleton.dev/docs/ssd"
					target="_blank"
				>
					Skeleton Docs.</a
				>
			</p>
		</div>
	</div>
	<div class="mx-[10%] my-8">
		<!-- Page Route Content -->
		<slot />
	</div>
</AppShell>
