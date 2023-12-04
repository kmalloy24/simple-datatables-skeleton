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
		<AppBar>
			<svelte:fragment slot="lead">
				<strong class="text-xl uppercase">Skeleton Headless Datatable</strong>
			</svelte:fragment>
			<svelte:fragment slot="trail">
				<a
					class="btn btn-sm variant-filled-primary"
					href="https://www.skeleton.dev/"
					target="_blank"
					rel="noreferrer"
				>
					Skeleton
				</a>
				<a
					class="btn btn-sm variant-filled-secondary"
					href="https://vincjo.fr/datatables/home"
					target="_blank"
					rel="noreferrer"
				>
					Svelte Simple Datatables
				</a>
				<a
					class="btn btn-sm variant-filled-tertiary"
					href="https://tailwindcss.com/"
					target="_blank"
					rel="noreferrer"
				>
					Tailwind
				</a>
				<a
					class="btn btn-sm variant-ghost-surface"
					href="https://github.com/kmalloy24/simple-datatables-skeleton"
					target="_blank"
					rel="noreferrer"
				>
					GitHub
				</a>
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>
	<!-- Page Route Content -->
	<slot />
</AppShell>
