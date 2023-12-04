<script>
	//Import data
	import data from '$lib/data';

	//Import local datatable components
	import Th from '$lib/components/Th.svelte';
	import ThFilter from '$lib/components/ThFilter.svelte';
	import Search from '$lib/components/Search.svelte';
	import RowsPerPage from '$lib/components/RowsPerPage.svelte';
	import RowCount from '$lib/components/RowCount.svelte';
	import Pagination from '$lib/components/Pagination.svelte';

	//Import datatable handler from Svelte Simple Datatables
	import { DataHandler } from '@vincjo/datatables';

	//Datatable handler initialization
	const handler = new DataHandler(data, { rowsPerPage: 10 });
	const rows = handler.getRows();
</script>

<header class="flex justify-between mt-4 mx-[10%]">
	<Search {handler} />
	<RowsPerPage {handler} />
</header>

<div class=" flex justify-center items-center mx-[10%]">
	<table class="table table-hover table-compact table-auto mt-4">
		<thead>
			<tr>
				<Th {handler} orderBy="first_name">First name</Th>
				<Th {handler} orderBy="last_name">Last name</Th>
				<Th {handler} orderBy="email">Email</Th>
			</tr>
			<tr>
				<ThFilter {handler} filterBy="first_name" />
				<ThFilter {handler} filterBy="last_name" />
				<ThFilter {handler} filterBy="email" />
			</tr>
		</thead>
		<tbody>
			{#each $rows as row}
				<tr>
					<td>{row.first_name}</td>
					<td>{row.last_name}</td>
					<td>{row.email}</td>
				</tr>
			{/each}
		</tbody>
	</table>
</div>

<footer class="flex justify-between mx-[10%]">
	<RowCount {handler} />
	<Pagination {handler} />
</footer>
