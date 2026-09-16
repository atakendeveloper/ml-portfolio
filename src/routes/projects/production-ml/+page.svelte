<script lang="ts">
	import SectionHeader from '$lib/components/SectionHeader.svelte';
	import TechTag from '$lib/components/TechTag.svelte';

	const tags = [
		'Python',
		'PyTorch',
		'Flask',
		'Dash',
		'SQL',
		'Docker',
		'Azure',
		'AVEVA PI',
		'Seeq',
		'RAG'
	];

	const capabilities = [
		{
			title: 'Production ML Inference',
			body:
				'Containerized machine-learning services deployed into production workflows for real-time engineering decisions.'
		},
		{
			title: 'Engineering Applications',
			body:
				'Full-stack internal applications connecting operational data, analytics, and writeback workflows for engineering teams.'
		},
		{
			title: 'Real-Time Analytics',
			body:
				'Manage-by-exception workflows, surveillance logic, and operational monitoring built around high-frequency industrial data.'
		},
		{
			title: 'Enterprise AI',
			body:
				'Retrieval-augmented engineering assistants and knowledge systems spanning multiple technical domains.'
		}
	];
</script>

<svelte:head>
	<title>Production ML & Industrial Analytics | Ashley Taken</title>
</svelte:head>

<section class="border-b border-gray-200 bg-white">
	<div class="page-shell py-16 md:py-20">
		<a
			href="/#projects"
			class="mb-6 inline-flex text-sm font-semibold text-gray-500 hover:text-gray-950"
		>
			← Back to projects
		</a>

		<div class="max-w-5xl">
			<div class="eyebrow">Production ML · Industrial AI · Engineering Analytics</div>

			<h1 class="mt-4 text-4xl font-black tracking-tight text-gray-950 md:text-5xl">
				Production ML & Industrial Analytics
			</h1>

			<p class="mt-6 max-w-4xl text-lg leading-8 text-gray-500">
				Production machine-learning systems, engineering applications, real-time analytics,
				and enterprise AI solutions built for complex industrial workflows.
			</p>

			<div class="mt-7 flex flex-wrap gap-2">
				{#each tags as tag}
					<TechTag label={tag} />
				{/each}
			</div>
		</div>
	</div>
</section>

<section class="page-shell py-16">
	<div class="grid gap-5 md:grid-cols-4">
		<div class="card p-5">
			<div class="metric-label">Domain</div>
			<div class="mt-2 font-bold text-gray-950">Offshore Energy</div>
		</div>

		<div class="card p-5">
			<div class="metric-label">Focus</div>
			<div class="mt-2 font-bold text-gray-950">Applied ML</div>
		</div>

		<div class="card p-5">
			<div class="metric-label">Environment</div>
			<div class="mt-2 font-bold text-gray-950">Production Systems</div>
		</div>

		<div class="card p-5">
			<div class="metric-label">Scope</div>
			<div class="mt-2 font-bold text-gray-950">ML + Full Stack + AI</div>
		</div>
	</div>
</section>

<section class="border-y border-gray-200 bg-white">
	<div class="page-shell py-16">
		<SectionHeader
			eyebrow="Selected Impact"
			title="Machine learning embedded into engineering workflows"
			description="The work spans predictive modeling, operational applications, real-time analytics, and enterprise AI rather than isolated model development."
		/>

		<div class="grid gap-5 md:grid-cols-2">
			<div class="card p-7">
				<div class="metric-label">Production Classification</div>

				<div class="mt-3 text-3xl font-black text-gray-950">
					77% → 98%
				</div>

				<p class="mt-3 text-sm leading-6 text-gray-500">
					Improved real-time well-status prediction accuracy by replacing legacy rule-based
					logic with a Dockerized 2D CNN inference workflow.
				</p>
			</div>

			<div class="card p-7">
				<div class="metric-label">Enterprise AI</div>

				<div class="mt-3 text-3xl font-black text-gray-950">
					22 Agents
				</div>

				<p class="mt-3 text-sm leading-6 text-gray-500">
					Architected an enterprise RAG ecosystem spanning multiple engineering domains with
					live-synced technical knowledge sources.
				</p>
			</div>
		</div>
	</div>
</section>

<section class="page-shell py-16">
	<SectionHeader
		eyebrow="Capabilities"
		title="End-to-end technical ownership"
		description="Projects were designed around operational use, not just model experimentation."
	/>

	<div class="grid gap-5 md:grid-cols-2 xl:grid-cols-4">
		{#each capabilities as item}
			<div class="card p-6">
				<h3 class="font-bold text-gray-950">{item.title}</h3>
				<p class="mt-3 text-sm leading-6 text-gray-500">{item.body}</p>
			</div>
		{/each}
	</div>
</section>

<section class="border-y border-gray-200 bg-white">
	<div class="page-shell py-16">
		<div class="grid gap-10 lg:grid-cols-[1fr_1fr]">
			<div>
				<SectionHeader
					eyebrow="Production ML"
					title="From model development to deployed inference"
					description="The production workflow included feature engineering, model training, containerized inference, operational integration, and monitoring."
				/>

				<p class="text-sm leading-6 text-gray-500">
					A 2D CNN classification pipeline was developed for real-time well-status inference
					using sliding windows, imbalance-aware training, confidence thresholds, and drift
					checks. The model was deployed in Dockerized Python services in Azure and integrated
					into operational workflows.
				</p>
			</div>

			<div class="card bg-gray-950 p-7 text-white">
				<div class="metric-label !text-gray-400">Production Flow</div>

				<div class="mt-6 space-y-3 text-sm">
					<div class="rounded-md border border-gray-700 bg-gray-900 p-4">
						Operational Time-Series Data
					</div>
					<div class="text-center text-gray-500">↓</div>
					<div class="rounded-md border border-gray-700 bg-gray-900 p-4">
						Feature / Window Construction
					</div>
					<div class="text-center text-gray-500">↓</div>
					<div class="rounded-md border border-gray-700 bg-gray-900 p-4">
						2D CNN Inference Service
					</div>
					<div class="text-center text-gray-500">↓</div>
					<div class="rounded-md border border-blue-700 bg-blue-950/40 p-4">
						Engineering Decision Support
					</div>
				</div>
			</div>
		</div>
	</div>
</section>

<section class="page-shell py-16">
	<div class="grid gap-8 lg:grid-cols-2">
		<div class="card p-7">
			<div class="eyebrow">Full-Stack Engineering</div>

			<h2 class="mt-3 text-2xl font-bold text-gray-950">
				Engineering applications connected to operational data
			</h2>

			<p class="mt-4 text-sm leading-6 text-gray-500">
				Built production engineering applications using Python, Flask, Dash, SQL, Docker, and
				Azure DevOps, including direct integration with AVEVA PI Asset Framework for
				engineering workflows and data writeback.
			</p>
		</div>

		<div class="card p-7">
			<div class="eyebrow">Operational Analytics</div>

			<h2 class="mt-3 text-2xl font-bold text-gray-950">
				Manage-by-exception surveillance
			</h2>

			<p class="mt-4 text-sm leading-6 text-gray-500">
				Developed real-time surveillance and exception-based monitoring workflows to reduce
				manual review and surface higher-value operational signals to engineering teams.
			</p>
		</div>
	</div>
</section>

<section class="border-y border-gray-200 bg-white">
	<div class="page-shell py-16">
		<SectionHeader
			eyebrow="Enterprise AI"
			title="Knowledge systems for technical engineering domains"
			description="Applied retrieval-augmented generation to make engineering knowledge easier to search, synthesize, and use."
		/>

		<div class="grid gap-5 md:grid-cols-3">
			<div class="card p-6">
				<div class="metric-label">Knowledge Sources</div>
				<div class="mt-2 font-bold text-gray-950">SharePoint + Network Drives</div>
			</div>

			<div class="card p-6">
				<div class="metric-label">Retrieval</div>
				<div class="mt-2 font-bold text-gray-950">Hybrid Search + Reranking</div>
			</div>

			<div class="card p-6">
				<div class="metric-label">Delivery</div>
				<div class="mt-2 font-bold text-gray-950">Domain-Specific Agents</div>
			</div>
		</div>

		<p class="mt-6 max-w-4xl text-sm leading-6 text-gray-500">
			The system used tailored prompts, multiple knowledge bases, and retrieval pipelines designed
			for different engineering contexts rather than one generic enterprise chatbot.
		</p>
	</div>
</section>

<section class="page-shell py-16">
	<div class="card p-8 md:p-10">
		<div class="eyebrow">Engineering Principles</div>

		<div class="mt-6 grid gap-8 md:grid-cols-3">
			<div>
				<h3 class="font-bold text-gray-950">Production-first design</h3>
				<p class="mt-2 text-sm leading-6 text-gray-500">
					Models are useful only when they integrate cleanly into operational systems and
					engineering workflows.
				</p>
			</div>

			<div>
				<h3 class="font-bold text-gray-950">Domain-aware ML</h3>
				<p class="mt-2 text-sm leading-6 text-gray-500">
					Engineering context, process behavior, and data quality constraints are treated as
					part of the modeling problem.
				</p>
			</div>

			<div>
				<h3 class="font-bold text-gray-950">End-to-end ownership</h3>
				<p class="mt-2 text-sm leading-6 text-gray-500">
					Projects span modeling, backend services, data integration, UI development,
					deployment, and production support.
				</p>
			</div>
		</div>
	</div>
</section>

<section class="border-t border-gray-200 bg-white">
	<div class="page-shell py-12">
		<div class="text-sm text-gray-500">
			Project details are intentionally generalized to respect employer confidentiality.
			Screenshots and additional visual examples will be added where appropriate.
		</div>
	</div>
</section>