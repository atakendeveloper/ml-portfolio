<script lang="ts">
	let {
		eyebrow,
		title,
		description
	}: {
		eyebrow: string;
		title: string;
		description?: string;
	} = $props();
</script>

<div class="mb-7 max-w-3xl">
	<div class="eyebrow mb-2">{eyebrow}</div>

	<h2 class="text-2xl font-bold tracking-tight text-gray-950 md:text-3xl">
		{title}
	</h2>

	{#if description}
		<p class="mt-3 leading-7 text-gray-500">
			{description}
		</p>
	{/if}
</div>