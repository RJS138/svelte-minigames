<script>
	import '../app.pcss';
	import Button from '$lib/components/ui/button/button.svelte';
	import { ModeWatcher, toggleMode } from 'mode-watcher';
	import MaterialSymbolsSunnyOutline from 'virtual:icons/material-symbols/sunny-outline';
	import MdiWeatherNight from 'virtual:icons/mdi/weather-night';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Home page" />
</svelte:head>

<Button on:click={toggleMode} variant="outline" size="icon">
	<MdiWeatherNight
		class="absolute h-[1.2rem] w-[1.2rem] scale-100 transition-all dark:rotate-0 dark:scale-0"
	/>
	<MaterialSymbolsSunnyOutline
		class="h-[1.2rem] w-[1.2rem] rotate-0 scale-0 transition-all dark:-rotate-90 dark:scale-100"
	/>
	<span class="sr-only">Toggle theme</span>
</Button>

<ModeWatcher />
<slot />
