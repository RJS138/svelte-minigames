<script lang="ts">
</script>

<h1 class=" flex items-center justify-center text-4xl">Tic Tac Toe</h1>

<section class=" mt-40 p-5">
	<div class="relative flex justify-center">
		<div class="board grid grid-cols-3" id="board">
			<div
				id="0"
				class="cell flex h-20 w-20 items-center justify-center text-3xl md:h-32 md:w-32"
			></div>
			<div
				id="1"
				class="cell flex h-20 w-20 items-center justify-center border-x border-black text-3xl dark:border-white md:h-32 md:w-32"
			></div>
			<div
				id="2"
				class="cell flex h-20 w-20 items-center justify-center text-3xl md:h-32 md:w-32"
			></div>
			<div
				id="3"
				class="cell flex h-20 w-20 items-center justify-center border-y border-black text-3xl dark:border-white md:h-32 md:w-32"
			></div>
			<div
				id="4"
				class="cell flex h-20 w-20 items-center justify-center border border-black text-3xl dark:border-white md:h-32 md:w-32"
			></div>
			<div
				id="5"
				class="cell flex h-20 w-20 items-center justify-center border-y border-black text-3xl dark:border-white md:h-32 md:w-32"
			></div>
			<div
				id="6"
				class="cell flex h-20 w-20 items-center justify-center text-3xl md:h-32 md:w-32"
			></div>
			<div
				id="7"
				class="cell flex h-20 w-20 items-center justify-center border-x border-black text-3xl dark:border-white md:h-32 md:w-32"
			></div>
			<div
				id="8"
				class="cell flex h-20 w-20 items-center justify-center text-3xl md:h-32 md:w-32"
			></div>
		</div>

		<div id="win-line"></div>
	</div>
</section>

<style>
</style>
