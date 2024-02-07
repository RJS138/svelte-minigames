<script lang="ts">
	import * as Table from '$lib/components/ui/table';
	import { root } from 'postcss';

	let board = [
		['', '', ''],
		['', '', ''],
		['', '', '']
	];

	function makeMove(row: number, col: number) {
		if (board[row][col] === '') {
			board[row][col] = 'X';
		}
	}
</script>

<h1>Tic Tac Toe</h1>

<Table.Root>
	{#each board as row, i}
		<Table.Row>
			{#each row as cell, j}
				<Table.Cell on:click={() => makeMove(i, j)}>{cell}</Table.Cell>
			{/each}
		</Table.Row>
	{/each}
</Table.Root>
