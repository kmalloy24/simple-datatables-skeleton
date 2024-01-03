<script lang="ts">
	import { DataHandler, type State, Datatable, Th } from '@vincjo/datatables/remote';
	import { reload } from './api';
	import ThFilter from '$lib/components/ssr/ThFilter.svelte';

	const handler = new DataHandler([], { rowsPerPage: 10, totalRows: 500 });
	const rows = handler.getRows();

	handler.onChange((state: State) => reload(state));

	handler.invalidate();
</script>

<Datatable {handler}>
	<table>
		<thead>
			<tr>
				<Th {handler} orderBy="id">ID</Th>
				<Th {handler} orderBy="name">Name</Th>
				<Th {handler} orderBy="email">Email</Th>
				<Th {handler} orderBy="body">Comment</Th>
			</tr>
			<tr>
				<ThFilter {handler} filterBy="id" />
				<ThFilter {handler} filterBy="name" />
				<ThFilter {handler} filterBy="email" />
				<ThFilter {handler} filterBy="body" />
			</tr>
		</thead>
		<tbody>
			{#each $rows as row}
				<tr>
					<td>{row.id}</td>
					<td><b>{row.name}</b></td>
					<td>{row.email}</td>
					<td><p>{row.body}</p></td>
				</tr>
			{/each}
		</tbody>
	</table>
</Datatable>
