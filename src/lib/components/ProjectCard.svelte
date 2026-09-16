<script lang="ts">
	import TechTag from './TechTag.svelte';

	let {
		number,
		title,
		subtitle,
		description,
		href,
		tags,
		accent = 'purple'
	}: {
		number: string;
		title: string;
		subtitle: string;
		description: string;
		href: string;
		tags: string[];
		accent?: 'purple' | 'blue' | 'dark';
	} = $props();

    function accentClass() {
        return {
            purple: 'bg-purple-600',
            blue: 'bg-blue-600',
            dark: 'bg-gray-900'
        }[accent];
    }
</script>

<a
	{href}
	class="card group flex h-full flex-col overflow-hidden transition duration-200 hover:-translate-y-1 hover:shadow-lg"
>
	<div class={`h-1.5 ${accentClass()}`}></div>

	<div class="flex flex-1 flex-col p-6">
		<div class="metric-label mb-5">
			Project {number}
		</div>

		<h3 class="text-xl font-bold text-gray-950">
			{title}
		</h3>

		<p class="mt-1 text-sm font-semibold text-purple-700">
			{subtitle}
		</p>

		<p class="mt-4 flex-1 text-sm leading-6 text-gray-500">
			{description}
		</p>

		<div class="mt-5 flex flex-wrap gap-2">
			{#each tags as tag}
				<TechTag label={tag} />
			{/each}
		</div>

		<div class="mt-6 flex items-center text-sm font-bold text-gray-900">
			View case study
			<span class="ml-2 transition-transform group-hover:translate-x-1">→</span>
		</div>
	</div>
</a>