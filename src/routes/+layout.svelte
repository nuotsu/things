<script lang="ts">
	import './app.css'

	let { children } = $props()
</script>

<svelte:head>
	<title>things from the internet</title>
	<meta name="description" content="cool things from the internet" />
	<link rel="icon" href="https://fav.farm/🥡" />
</svelte:head>

<main class="flex min-h-svh flex-wrap items-end justify-center">
	{@render children()}
</main>
