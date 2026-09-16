<script lang="ts">
	const sections = [
		{
			label: 'Machine Learning',
			items: [
				'PyTorch',
				'XGBoost',
				'Transformers',
				'CNNs',
				'LSTMs',
				'Time-Series Forecasting',
				'Anomaly Detection',
				'Representation Learning'
			]
		},
		{
			label: 'Applied AI',
			items: [
				'RAG',
				'Agentic AI',
				'Hybrid Retrieval',
				'BM25',
				'Cross-Encoder Reranking',
				'MCP',
				'LLM Evaluation'
			]
		},
		{
			label: 'Engineering',
			items: [
				'Python',
				'SQL',
				'FastAPI',
				'Flask',
				'SvelteKit',
				'Docker',
				'Azure',
				'AWS',
				'Redis',
				'MariaDB'
			]
		}
	];
</script>

<svelte:head>
	<title>Resume | Ashley Taken</title>
</svelte:head>

<section class="border-b border-gray-200 bg-white">
	<div class="page-shell py-16">
		<div class="max-w-3xl">
			<div class="eyebrow">Resume</div>

			<h1 class="mt-3 text-4xl font-black tracking-tight text-gray-950 md:text-5xl">
				Ashley Taken
			</h1>

			<p class="mt-4 text-lg leading-8 text-gray-500">
				Machine Learning Engineer · Data Scientist · Applied AI
			</p>

			<div class="mt-7 flex flex-wrap gap-3">
				<a
					href="/experience"
					class="rounded-md bg-gray-900 px-5 py-3 text-sm font-bold text-white hover:bg-gray-700"
				>
					View Experience
				</a>

				<a
					href="/contact"
					class="rounded-md border border-gray-300 bg-white px-5 py-3 text-sm font-bold text-gray-800 hover:bg-gray-50"
				>
					Contact
				</a>
			</div>
		</div>
	</div>
</section>

<section class="page-shell py-14">
	<div class="grid gap-6 lg:grid-cols-[1.2fr_0.8fr]">
		<div class="space-y-6">
			<div class="card p-7">
				<div class="eyebrow">Profile</div>

				<p class="mt-4 leading-7 text-gray-600">
					Machine learning engineer with experience spanning production ML, quantitative
					research, industrial AI, full-stack engineering, and agentic AI systems. Background
					in chemical engineering and analytics with a focus on building rigorous, deployable
					technical systems.
				</p>
			</div>

			<div class="card p-7">
				<div class="eyebrow">Education</div>

				<div class="mt-5 space-y-6">
					<div>
						<div class="font-bold text-gray-950">
							M.S. Analytics · Computational Track
						</div>
						<div class="mt-1 text-sm text-gray-500">
							Georgia Institute of Technology · 2025
						</div>
					</div>

					<div>
						<div class="font-bold text-gray-950">
							B.S. Chemical & Biomolecular Engineering
						</div>
						<div class="mt-1 text-sm text-gray-500">
							University of Houston · 2017
						</div>
					</div>

					<div>
						<div class="font-bold text-gray-950">
							B.S. Biology · Minor in Psychology
						</div>
						<div class="mt-1 text-sm text-gray-500">
							Texas A&M University · 2014
						</div>
					</div>
				</div>
			</div>
		</div>

		<div class="card p-7">
			<div class="eyebrow">Technical Skills</div>

			<div class="mt-6 space-y-7">
				{#each sections as section}
					<div>
						<div class="text-sm font-bold text-gray-950">
							{section.label}
						</div>

						<div class="mt-3 flex flex-wrap gap-2">
							{#each section.items as item}
								<span
									class="rounded-md border border-gray-200 bg-gray-50 px-2.5 py-1 text-xs font-semibold text-gray-600"
								>
									{item}
								</span>
							{/each}
						</div>
					</div>
				{/each}
			</div>
		</div>
	</div>
</section>

<section class="border-t border-gray-200 bg-white">
	<div class="page-shell py-12">
		<p class="text-sm text-gray-500">
			A downloadable PDF résumé can be added here before final publication.
		</p>
	</div>
</section>