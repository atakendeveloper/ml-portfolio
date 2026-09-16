<script lang="ts">
	import TechTag from '$lib/components/TechTag.svelte';

	const roles = [
		{
			company: 'Occidental Petroleum (Oxy)',
			title: 'Data Scientist',
			dates: '2024 – Present',
			type: 'Contract · Remote',
			points: [
				'Deployed Dockerized 2D CNN inference services in Azure, improving real-time well-status prediction accuracy from 77% to 98%.',
				'Built full-stack engineering applications using Python, Flask, Dash, SQL, Docker, Azure DevOps, and AVEVA PI.',
				'Architected a 22-agent enterprise RAG ecosystem across multiple engineering domains.',
				'Created and maintained 25+ production manage-by-exception workflows across Seeq, Power Automate, Azure, and AVEVA PI for offshore operations.'
			],
			tags: ['Python', 'PyTorch', 'Azure', 'Docker', 'AVEVA PI', 'RAG']
		},
		{
			company: 'Taken Group LLC',
			title: 'Founder / Machine Learning Engineer',
			dates: '2024 – Present',
			type: 'Independent R&D',
			points: [
				'Built a full-stack quantitative ML research platform using FastAPI, SvelteKit, MariaDB, Redis, Docker, and Python.',
				'Developed reproducible statistical research workflows for sampling, feature engineering, leakage-aware validation, and model evaluation.',
				'Built an agentic research platform with hybrid retrieval, reranking, MCP tooling, and a dedicated evaluation framework.',
				'Developed transformer and contrastive-learning workflows for financial time-series representation learning.'
			],
			tags: ['FastAPI', 'SvelteKit', 'PyTorch', 'Agents', 'Time Series']
		},
		{
			company: 'Imubit',
			title: 'Implementation Engineer (Forward Deployed Engineer)',
			dates: '2022 – 2024',
			type: 'Industrial AI',
			points: [
				'Designed and deployed five closed-loop reinforcement-learning systems from POC to production across industrial process applications.',
				'Analyzed model behavior and supported production tuning using SHAP, hyperparameter optimization, YAML deployment configuration, Grafana, and cloud infrastructure.',
				'Delivered projects producing more than $2M in documented value.'
			],
			tags: ['Reinforcement Learning', 'SHAP', 'AWS', 'Grafana']
		},
        {
            company: 'Chevron Phillips Chemical',
            title: 'Process / Operations / Advanced Process Control Engineer',
            dates: '2020 – 2022',
            type: 'Chemical Engineering',
            points: [
                'Developed and supported advanced process control and real-time optimization applications across olefins operations.',
                'Automated real-time furnace monitoring with Python by generating custom status signals and operator alerts to improve response time.',
                'Modernized plant data analysis using Python regression models for distillation quality control and production optimization.',
                'Built real-time and forecasted emissions dashboards using Python and Power BI to help prevent EPA compliance violations across three plants.',
                'Identified approximately $350K/year in nitrogen savings through condition-based analysis of a closed-loop regeneration system.'
            ],
            tags: ['Python', 'APC', 'Seeq', 'Power BI', 'Process Engineering']
        }
	];
</script>

<svelte:head>
	<title>Experience | Ashley Taken</title>
</svelte:head>

<section class="border-b border-gray-200 bg-white">
	<div class="page-shell py-12">
		<div class="mb-5 flex flex-wrap items-center gap-3">
			<a
				href="/"
				class="inline-flex text-sm font-semibold text-gray-500 transition hover:text-gray-950"
			>
				← Back
			</a>

			<a
				href="/Ashley-Taken-Resume.pdf"
				target="_blank"
				rel="noopener noreferrer"
				class="rounded-md border border-purple-200 bg-purple-50 px-4 py-2 text-sm font-bold text-purple-800 transition hover:bg-purple-100"
			>
				Resume PDF
			</a>
		</div>

		<div class="eyebrow">Experience</div>

		<h1 class="mt-3 text-4xl font-black tracking-tight text-gray-950">
			Machine learning, AI, and engineering
		</h1>

		<p class="mt-4 max-w-2xl text-lg text-gray-500">
			Experience spanning production ML, quantitative research, industrial AI, and process engineering.
		</p>
	</div>
</section>

<section class="page-shell py-14">
	<div class="space-y-5">
		{#each roles as role}
			<div class="card p-7">
				<div class="grid gap-6 lg:grid-cols-[260px_1fr]">
					<div>
						<div class="text-xl font-bold text-gray-950">{role.company}</div>
						<div class="mt-1 text-sm font-semibold text-purple-700">{role.title}</div>
						<div class="mt-3 text-sm text-gray-500">{role.dates}</div>
						<div class="text-xs text-gray-400">{role.type}</div>
					</div>

					<div>
						<ul class="space-y-3 text-sm leading-6 text-gray-600">
							{#each role.points as point}
								<li class="flex gap-3">
									<span class="mt-2 h-1.5 w-1.5 shrink-0 rounded-full bg-purple-600"></span>
									<span>{point}</span>
								</li>
							{/each}
						</ul>

						<div class="mt-5 flex flex-wrap gap-2">
							{#each role.tags as tag}
								<TechTag label={tag} />
							{/each}
						</div>
					</div>
				</div>
			</div>
		{/each}
	</div>
</section>