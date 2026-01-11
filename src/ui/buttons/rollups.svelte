<script lang="ts">
	let hovered = $state(false)
	let t = $state<ReturnType<typeof setTimeout> | undefined>(undefined)

	const duration = 600

	function onenter() {
		if (hovered) return

		hovered = true
		if (t) clearTimeout(t)
		t = setTimeout(() => (hovered = false), duration)
	}
</script>

<a
	class="relative inline-flex overflow-clip px-ch text-[#e4eac8]"
	class:hovered
	style:--rollups-duration="{duration}ms"
	href="https://rollups.com"
	onmouseenter={onenter}
	ontouchstart={onenter}
>
	Terms of Service
</a>

<style>
	@property --rollups-bar {
		syntax: '<length>';
		initial-value: 0;
		inherits: true;
	}

	a {
		background: linear-gradient(268deg, #295d32 4.2%, #273f2c 98.63%);

		&::after {
			--rollups-bar: 1ch;
			content: '';
			pointer-events: none;
			position: absolute;
			inset: 0 auto 0 calc(var(--rollups-bar) * -1);
			z-index: 1;
			width: var(--rollups-bar);
			background: currentColor;
		}

		&.hovered::after {
			animation: scan var(--rollups-duration) ease-in-out;
		}
	}

	@keyframes scan {
		45% {
			--rollups-bar: 4ch;
		}

		100% {
			--rollups-bar: 0;
			left: 100%;
		}
	}
</style>
