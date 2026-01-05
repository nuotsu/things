<script lang="ts">
	let disableHref = $state(true)

	$effect(() => {
		document.querySelectorAll('main a[href]').forEach((link) => {
			if (!link.hasAttribute('data-href')) {
				;(link as HTMLElement).dataset.href = link.getAttribute('href')!
			}

			if (disableHref) {
				link.setAttribute('href', '#')
				link.removeAttribute('target')
			} else {
				link.setAttribute('href', (link as HTMLElement).dataset.href!)
				link.setAttribute('target', '_blank')
			}
		})
	})
</script>

<svelte:window
	on:keydown={(e) => {
		if (e.key === 'h') disableHref = !disableHref
	}}
/>

<label>
	<input id="disable-href" type="checkbox" bind:checked={disableHref} />
	<span>Disable <code><kbd>h</kbd>ref</code></span>
</label>
