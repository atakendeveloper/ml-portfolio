<script lang="ts">
	let { label }: { label: string } = $props();
</script>

<span
	class="inline-flex items-center rounded-md border border-gray-200 bg-gray-50 px-2.5 py-1 text-xs font-semibold text-gray-600"
>
	{label}
</span>