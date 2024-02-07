<script lang="ts">
</script>

<h1>Tic Tac Toe</h1>

<div
	class="flex flex-wrap h-full justify-center content-center max-w-2xl bg-slate-50"
	id="gameboard"
>
	<div class="h-56 w-56 border-r-4 border-b-4 flex items-center justify-center" id="0"></div>
	<div
		class="h-56 w-56 border-r-4 border-b-4 flex items-center justify-center bg-transparent"
		id="1"
	></div>
	<div class="h-56 w-56 border-b-4 flex items-center justify-center bg-transparent" id="2"></div>
	<div
		class="h-56 w-56 border-b-4 border-r-4 flex items-center justify-center bg-transparent"
		id="3"
	></div>
	<div
		class="h-56 w-56 border-b-4 border-r-4 flex items-center justify-center bg-transparent"
		id="4"
	></div>
	<div class="h-56 w-56 border-b-4 flex items-center justify-center bg-transparent" id="5"></div>
	<div class="h-56 w-56 border-r-4 flex items-center justify-center bg-transparent" id="6"></div>
	<div class="h-56 w-56 border-r-4 flex items-center justify-center bg-transparent" id="7"></div>
	<div class="h-56 w-56 flex items-center justify-center bg-transparent" id="8"></div>
</div>

<!-- <style>
	.box {
		height: 150px;
		width: 150px;
		color: #0b9d43;
		border-right: 2px solid;
		border-bottom: 2px solid;
	}

	.box:nth-child(3n) {
		border-right: none;
	}
	.box:nth-last-child(-n + 3) {
		border-bottom: none;
	}

	#gameboard div {
		background-color: #f0f0f0;
		display: flex;
		justify-content: center;
		align-items: center;
		font-size: 2em;
		cursor: pointer;
	}

	#gameboard div:hover {
		background-color: #e0e0e0;
	}
</style> -->
