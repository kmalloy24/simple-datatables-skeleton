<script lang="ts">
	import { DataHandler, type State, Datatable, Th, ThFilter } from '@vincjo/datatables/remote';
	import { reload } from './api';

	const handler = new DataHandler([], { rowsPerPage: 10 });
	const rows = handler.getRows();

	handler.onChange((state: State) => reload(state));

	handler.invalidate();
</script>

<Datatable {handler}>
	<table>
		<thead>
			<tr>
				<th>ID</th>
				<th>Avatar</th>
				<th>First name</th>
				<th>Last name</th>
				<th>Age</th>
				<th>Gender</th>
				<th>Height / Weight</th>
			</tr>
		</thead>
		<tbody>
			{#each $rows as row}
				<tr>
					<td>{row.id}</td>
					<td>
						<img src={row.image} alt="avatar" class="w-8" />
					</td>
					<td>{row.firstName}</td>
					<td>{row.lastName}</td>
					<td>{row.age}</td>
					<td>{row.gender}</td>
					<td>
						{row.height / 100}m / {row.weight}kg
					</td>
				</tr>
			{/each}
		</tbody>
	</table>
</Datatable>
