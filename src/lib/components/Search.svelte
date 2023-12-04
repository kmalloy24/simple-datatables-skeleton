<script lang="ts">
	import type { DataHandler } from '@vincjo/datatables';
	export let handler: DataHandler;
	let value = '';
</script>

<input
	class="input w-64"
	type="search"
	placeholder="Search..."
	bind:value
	on:input={() => handler.search(value)}
/>
