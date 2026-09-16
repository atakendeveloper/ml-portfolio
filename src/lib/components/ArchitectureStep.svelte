<script lang="ts">
	let {
		number,
		title,
		description,
		accent = 'purple'
	}: {
		number: string;
		title: string;
		description: string;
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

<div class={`rounded-lg border-l-4 p-5 ${accentClass}`}>
	<div class="metric-label">{number}</div>
	<div class="mt-2 font-bold text-gray-950">{title}</div>
	<div class="mt-2 text-sm leading-6 text-gray-500">
		{description}
	</div>
</div>