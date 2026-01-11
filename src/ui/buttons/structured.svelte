<a class="relative font-extralight text-white" href="https://structured.money"> mint maxBTC </a>

<style>
	a {
		--inset: 1.5ch;
		padding: 6px 2em;

		&::before {
			content: '';
			position: absolute;
			inset: 0 0.5ch;
			z-index: -1;
			background: black;
			clip-path: polygon(
				0 50%,
				var(--inset) 0%,
				calc(100% - var(--inset)) 0%,
				100% 50%,
				calc(100% - var(--inset)) 100%,
				var(--inset) 100%,
				0 50%
			);
		}

		&::after {
			content: '';
			position: absolute;
			inset: 0 1.5ch;
			z-index: -1;
			background: #000;
			border-radius: 1lh;
			transition: 0.3s ease-in-out;
			transition-property: border-radius, inset;
		}

		&:hover::after {
			inset-inline: 0;
			border-radius: 4px;
		}
	}
</style>
