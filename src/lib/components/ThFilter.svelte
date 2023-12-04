<script lang="ts">
	import type { DataHandler, Field } from '@vincjo/datatables';
	export let handler: DataHandler;
	export let filterBy = null;
	let value = '';
</script>

<th>
	<input
		class="input variant-form-material h-8 text-sm w-64"
		type="text"
		placeholder="Filter"
		bind:value
		on:input={() => {
			if (filterBy) {
				handler.filter(value, filterBy);
			}
		}}
	/>
</th>
