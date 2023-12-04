<script lang="ts">
	import type { DataHandler } from '@vincjo/datatables';
	export let handler: DataHandler;
	const pageNumber = handler.getPageNumber();
	const pageCount = handler.getPageCount();
	const pages = handler.getPages({ ellipsis: true });
</script>

<section class="my-2 btn-group variant-ghost-surface [&>*+*]:border-surface-500">
	<button
		type="button"
		class:disabled={$pageNumber === 1}
		on:click={() => handler.setPage('previous')}
	>
		Previous
	</button>
	{#each $pages as page}
		<button
			type="button"
			class:active={$pageNumber === page}
			class:ellipse={page === null}
			on:click={() => handler.setPage(page)}
		>
			{page ?? '...'}
		</button>
	{/each}
	<button
		type="button"
		class:disabled={$pageNumber === $pageCount}
		on:click={() => handler.setPage('next')}
	>
		Next
	</button>
</section>
