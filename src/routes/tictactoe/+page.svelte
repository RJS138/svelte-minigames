<script lang="ts">
	import Button from '$lib/components/ui/button/button.svelte';

	let winLine: HTMLElement;
	let cell: Array<HTMLElement> = [];
	$: currentPlayer = 'X';
	$: board = Array(9).fill('');
	$: winner = '';
	$: winLine;
	$: cell;

	function hoverEffect(index: number) {
		if (board[index] !== '' || winner) return;
		// Put an opactiy 50 current player on the cell
		cell[index].textContent = currentPlayer;
		cell[index].style.color = '255, 255, 255, 0.5';
	}

	function removeHoverEffect(index: number) {
		if (board[index] !== '' || winner) return;
		// Remove the opacity 50 current player on the cell
		cell[index].textContent = '';
		cell[index].style.textRendering;
	}

	function resetGame() {
		board = Array(9).fill('');
		winner = '';
		if (winLine) {
			winLine.style.opacity = '0';
		}
		currentPlayer = 'X';
		// Loop over each cell and run the removeHoverEffect function
		cell.forEach((cell) => {
			removeHoverEffect(Number(cell.id));
		});
	}

	function handleCellClick(index: number) {
		// If the cell is not empty, return
		if (board[index] !== '' || winner) return;
		// Set the cell value
		board[index] = currentPlayer;
		cell[index].style.opacity = '1';
		// Check for winner
		checkWinner();
		// Switch player
		currentPlayer = currentPlayer === 'X' ? 'O' : 'X';
	}
	function checkWinner() {
		const winningCombos = [
			[0, 1, 2],
			[3, 4, 5],
			[6, 7, 8],
			[0, 3, 6],
			[1, 4, 7],
			[2, 5, 8],
			[0, 4, 8],
			[2, 4, 6]
		];
		for (let i = 0; i < winningCombos.length; i++) {
			const [a, b, c] = winningCombos[i];
			if (board[a] && board[a] === board[b] && board[a] === board[c]) {
				winner = board[a];
				if (winLine) {
					winLine.style.opacity = '1';
					winLine.textContent = `${currentPlayer} Wins!`;
					winLine.style.color = currentPlayer === 'X' ? 'red' : 'blue';
				}
			}
		}
		if (!board.includes('') && !winner) {
			winner = 'draw';
			if (winLine) {
				winLine.style.opacity = '1';
				winLine.textContent = 'Draw!';
				winLine.style.color = 'green';
			}
		}
	}
</script>

<svelte:head>
	<title>Tic-Tac-Toe</title>
	<meta name="description" content="Tic-Tac-Toe game" />
</svelte:head>

<h1 class=" flex items-center justify-center text-4xl">Tic-Tac-Toe</h1>
<div class="m-5 flex items-center justify-center">
	<Button on:click={resetGame}>Reset</Button>
</div>

<h2 class="flex items-center justify-center text-2xl">Current Player: {currentPlayer}</h2>

<div bind:this={winLine} class="mt-5 flex items-center justify-center text-3xl opacity-0"></div>

<section class=" m-5 p-5">
	<div class="relative flex justify-center">
		<div class="board grid grid-cols-3" id="board">
			<button
				id="0"
				class="cell dark:hover: flex h-20 w-20 items-center justify-center text-8xl md:h-32 md:w-32"
				bind:this={cell[0]}
				on:focus={() => hoverEffect(0)}
				on:blur={() => removeHoverEffect(0)}
				on:mouseover={() => hoverEffect(0)}
				on:mouseout={() => removeHoverEffect(0)}
				on:click={() => handleCellClick(0)}
				on:keydown={(event) => {
					if (event.key === 'Enter' || event.key === ' ') {
						handleCellClick(0);
					}
				}}>{board[0]}</button
			>
			<button
				id="1"
				class="cell flex h-20 w-20 items-center justify-center border-x border-black text-8xl dark:border-white md:h-32 md:w-32"
				bind:this={cell[1]}
				on:focus={() => hoverEffect(1)}
				on:blur={() => removeHoverEffect(1)}
				on:mouseover={() => hoverEffect(1)}
				on:mouseout={() => removeHoverEffect(1)}
				on:click={() => handleCellClick(1)}
				on:keydown={(event) => {
					if (event.key === 'Enter' || event.key === ' ') {
						handleCellClick(1);
					}
				}}>{board[1]}</button
			>
			<button
				id="2"
				class="cell flex h-20 w-20 items-center justify-center text-8xl md:h-32 md:w-32"
				bind:this={cell[2]}
				on:focus={() => hoverEffect(2)}
				on:blur={() => removeHoverEffect(2)}
				on:mouseover={() => hoverEffect(2)}
				on:mouseout={() => removeHoverEffect(2)}
				on:click={() => handleCellClick(2)}
				on:keydown={(event) => {
					if (event.key === 'Enter' || event.key === ' ') {
						handleCellClick(2);
					}
				}}>{board[2]}</button
			>
			<button
				id="3"
				class="cell flex h-20 w-20 items-center justify-center border-y border-black text-8xl dark:border-white md:h-32 md:w-32"
				bind:this={cell[3]}
				on:focus={() => hoverEffect(3)}
				on:blur={() => removeHoverEffect(3)}
				on:mouseover={() => hoverEffect(3)}
				on:mouseout={() => removeHoverEffect(3)}
				on:click={() => handleCellClick(3)}
				on:keydown={(event) => {
					if (event.key === 'Enter' || event.key === ' ') {
						handleCellClick(3);
					}
				}}>{board[3]}</button
			>
			<button
				id="4"
				class="cell flex h-20 w-20 items-center justify-center border border-black text-8xl dark:border-white md:h-32 md:w-32"
				bind:this={cell[4]}
				on:focus={() => hoverEffect(4)}
				on:blur={() => removeHoverEffect(4)}
				on:mouseover={() => hoverEffect(4)}
				on:mouseout={() => removeHoverEffect(4)}
				on:click={() => handleCellClick(4)}
				on:keydown={(event) => {
					if (event.key === 'Enter' || event.key === ' ') {
						handleCellClick(4);
					}
				}}>{board[4]}</button
			>
			<button
				id="5"
				class="cell flex h-20 w-20 items-center justify-center border-y border-black text-8xl dark:border-white md:h-32 md:w-32"
				bind:this={cell[5]}
				on:focus={() => hoverEffect(5)}
				on:blur={() => removeHoverEffect(5)}
				on:mouseover={() => hoverEffect(5)}
				on:mouseout={() => removeHoverEffect(5)}
				on:click={() => handleCellClick(5)}
				on:keydown={(event) => {
					if (event.key === 'Enter' || event.key === ' ') {
						handleCellClick(5);
					}
				}}>{board[5]}</button
			>
			<button
				id="6"
				class="cell flex h-20 w-20 items-center justify-center text-8xl md:h-32 md:w-32"
				bind:this={cell[6]}
				on:focus={() => hoverEffect(6)}
				on:blur={() => removeHoverEffect(6)}
				on:mouseover={() => hoverEffect(6)}
				on:mouseout={() => removeHoverEffect(6)}
				on:click={() => handleCellClick(6)}
				on:keydown={(event) => {
					if (event.key === 'Enter' || event.key === ' ') {
						handleCellClick(6);
					}
				}}>{board[6]}</button
			>
			<button
				id="7"
				class="cell flex h-20 w-20 items-center justify-center border-x border-black text-8xl dark:border-white md:h-32 md:w-32"
				bind:this={cell[7]}
				on:focus={() => hoverEffect(7)}
				on:blur={() => removeHoverEffect(7)}
				on:mouseover={() => hoverEffect(7)}
				on:mouseout={() => removeHoverEffect(7)}
				on:click={() => handleCellClick(7)}
				on:keydown={(event) => {
					if (event.key === 'Enter' || event.key === ' ') {
						handleCellClick(7);
					}
				}}>{board[7]}</button
			>
			<button
				id="8"
				class="cell flex h-20 w-20 items-center justify-center text-8xl md:h-32 md:w-32"
				bind:this={cell[8]}
				on:focus={() => hoverEffect(8)}
				on:blur={() => removeHoverEffect(8)}
				on:mouseover={() => hoverEffect(8)}
				on:mouseout={() => removeHoverEffect(8)}
				on:click={() => handleCellClick(8)}
				on:keydown={(event) => {
					if (event.key === 'Enter' || event.key === ' ') {
						handleCellClick(8);
					}
				}}>{board[8]}</button
			>
		</div>
	</div>
</section>

<style>
</style>
