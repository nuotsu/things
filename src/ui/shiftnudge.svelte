<script lang="ts"></script>

<a
	href="https://shiftnudge.com"
	target="_blank"
	style:--accent="#f06"
	style:--bg="#0f0e0f"
	class="group relative inline-flex overflow-clip bg-(--bg) text-(--accent)"
>
	<div
		class="inline-flex min-w-[10ch] grow py-[.25ch] pr-ch transition-all group-not-hover:translate-x-[-2ch] group-hover:bg-(--accent) group-hover:text-(--bg)"
	>
		{@render arrow()}
		<span class="grow">Apply</span>
	</div>

	{@render arrow(
		'absolute inset-y-0 right-0 m-auto group-hover:translate-x-[2ch] transition-transform',
	)}
</a>

{#snippet arrow(className?: string)}
	<svg
		class="{className} shrink-0"
		xmlns="http://www.w3.org/2000/svg"
		width="24"
		height="24"
		viewBox="0 0 24 24"
	>
		<path
			fill="none"
			stroke="currentColor"
			stroke-linecap="square"
			stroke-width="2"
			d="m13 17.5l5.5-5.5L13 6.5m4.25 5.5h-13"
		/>
	</svg>
{/snippet}
