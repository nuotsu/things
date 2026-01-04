<script lang="ts">
	import DisableHref from './disable-href.svelte'

	let open = $state(false)
</script>

<svelte:window
	on:keydown={(e) => {
		if (e.key === 'c') open = !open
	}}
/>

<details
	class="group absolute right-0 bottom-0"
	onmouseenter={() => (open = true)}
	onmouseleave={() => (open = false)}
	bind:open
>
	<summary class="group-not-open:px-ch" aria-label="Controls">
		<span class="group-not-has-checked:hidden">*</span>
	</summary>

	<fieldset>
		<DisableHref />
	</fieldset>
</details>
