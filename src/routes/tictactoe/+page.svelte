<script lang="ts">
</script>

<h1 class=" text-4xl flex items-center justify-center">Tic Tac Toe</h1>

<section class=" mt-40 p-5">
	<div class="flex justify-center relative">
		<div class="board grid grid-cols-3" id="board">
			<div
				id="0"
				class="cell w-20 h-20 md:w-32 md:h-32 text-3xl flex items-center justify-center"
			></div>
			<div
				id="1"
				class="cell border-x border-black dark:border-white w-20 h-20 md:w-32 md:h-32 text-3xl flex items-center justify-center"
			></div>
			<div
				id="2"
				class="cell w-20 h-20 md:w-32 md:h-32 text-3xl flex items-center justify-center"
			></div>
			<div
				id="3"
				class="cell border-y border-black dark:border-white w-20 h-20 md:w-32 md:h-32 text-3xl flex items-center justify-center"
			></div>
			<div
				id="4"
				class="cell border border-black dark:border-white w-20 h-20 md:w-32 md:h-32 text-3xl flex items-center justify-center"
			></div>
			<div
				id="5"
				class="cell border-y border-black dark:border-white w-20 h-20 md:w-32 md:h-32 text-3xl flex items-center justify-center"
			></div>
			<div
				id="6"
				class="cell w-20 h-20 md:w-32 md:h-32 text-3xl flex items-center justify-center"
			></div>
			<div
				id="7"
				class="cell border-x border-black dark:border-white w-20 h-20 md:w-32 md:h-32 text-3xl flex items-center justify-center"
			></div>
			<div
				id="8"
				class="cell w-20 h-20 md:w-32 md:h-32 text-3xl flex items-center justify-center"
			></div>
		</div>

		<div id="win-line"></div>
	</div>
</section>
