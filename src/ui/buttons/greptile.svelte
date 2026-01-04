<script lang="ts"></script>

<a
	href="https://www.greptile.com"
	target="_blank"
	class="relative inline-flex min-w-[20ch] items-center justify-center gap-ch bg-[#107a4d] p-ch font-mono text-xs text-white"
>
	Try for free

	<svg class="size-4" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24">
		<path
			fill="none"
			stroke="currentColor"
			stroke-linecap="square"
			stroke-width="2"
			d="m13 17.5l5.5-5.5L13 6.5m4.25 5.5h-13"
		/>
	</svg>
</a>

<style>
	@property --x {
		syntax: '<percentage>';
		initial-value: 0%;
		inherits: true;
	}

	a {
		&::before,
		&::after {
			content: '';
			position: absolute;
			inset: 0;
			mask: linear-gradient(135deg, #000, #000 var(--x), transparent var(--x));
			transition: --x 0.5s linear;
		}

		&:hover {
			--x: 100%;
		}
	}

	a::before {
		background: left / 1ch 100%
			repeating-linear-gradient(
				to right,
				transparent,
				transparent calc(1ch - 1px),
				#fff4 calc(1ch - 1px),
				#fff4 1ch
			);
		transition-duration: 1s;
	}

	a::after {
		background: top / 1ch 100%
			repeating-linear-gradient(
				to bottom,
				transparent,
				transparent calc(1ch - 1px),
				#fff4 calc(1ch - 1px),
				#fff4 1ch
			);
	}
</style>
