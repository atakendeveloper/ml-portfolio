<script lang="ts">
	let {
		src,
		alt,
		title,
		caption
	}: {
		src: string;
		alt: string;
		title: string;
		caption?: string;
	} = $props();
</script>

<figure class="card overflow-hidden">
	<div class="border-b border-gray-200 bg-gray-50 px-5 py-4">
		<div class="text-sm font-bold text-gray-950">{title}</div>

		{#if caption}
			<div class="mt-1 text-xs leading-5 text-gray-500">
				{caption}
			</div>
		{/if}
	</div>

	<div class="bg-white p-3">
		<img
			{src}
			{alt}
			class="w-full rounded-md border border-gray-200 object-contain"
		/>
	</div>
</figure>