<script lang="ts">
	import { page } from '$app/state';

	const nav = [
		{ label: 'Projects', href: '/#projects' },
		{ label: 'Experience', href: '/experience' },
		{ label: 'Resume', href: '/resume' },
		{ label: 'Contact', href: '/contact' }
	];
</script>

<header class="sticky top-0 z-50 border-b border-gray-200 bg-white/95 backdrop-blur">
	<div class="page-shell flex h-16 items-center justify-between">
		<a href="/" class="flex items-center gap-3">
			<div
				class="flex h-9 w-9 items-center justify-center rounded-lg bg-gray-900 text-sm font-black text-white"
			>
				AT
			</div>

			<div class="leading-tight">
				<div class="font-bold text-gray-900">Ashley Taken</div>
				<div class="text-xs text-gray-500">Machine Learning Engineer</div>
			</div>
		</a>

		<nav class="hidden items-center gap-1 md:flex">
			{#each nav as item}
				<a
					href={item.href}
					class="rounded-md px-3 py-2 text-sm font-medium text-gray-600 transition hover:bg-gray-100 hover:text-gray-950"
				>
					{item.label}
				</a>
			{/each}
		</nav>
	</div>
</header>