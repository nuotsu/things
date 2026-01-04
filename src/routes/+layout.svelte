<script lang="ts">
	import './app.css'
	import Controls from '$ui/controls/details.svelte'

	let { children } = $props()
</script>

<svelte:head>
	<title>things from the internet</title>
	<meta name="description" content="cool things from the internet" />
	<link rel="icon" href="https://fav.farm/🥡" />
</svelte:head>

<main class="flex min-h-svh flex-wrap place-content-center items-center gap-ch">
	{@render children()}
</main>

<Controls />
