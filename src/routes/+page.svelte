<script>
	import Button from '$lib/components/ui/button/button.svelte';
</script>

<h1>Home</h1>

<ul>
	<li>
		<Button class="bg-slate-500" href="/tictactoe">Tic Tac Toe</Button>
		<Button class="bg-slate-500 " href="/sudoku">Sudoku</Button>
		<Button class="bg-slate-500" href="/idleclicker">Idle Clicker</Button>
	</li>
</ul>

<style>
	h1 {
		display: flex;
		justify-content: center;
	}
	li {
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
	}
</style>
