<script lang="ts">
	import TechTag from '$lib/components/TechTag.svelte';

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
					href="/Ashley-Taken-Resume.pdf"
					download="Ashley-Taken-Resume.pdf"
					class="rounded-md bg-gray-900 px-5 py-3 text-sm font-bold !text-white hover:bg-gray-700"
				>
					Download Resume
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

<div class="page-shell space-y-10 py-14">
<div class="grid gap-6 lg:grid-cols-2">
    <section aria-labelledby="profile">
        <div class="card h-full p-7">
            <h2 id="profile" class="eyebrow">Professional Summary</h2>

            <p class="mt-4 leading-7 text-gray-600">
                Machine Learning Engineer and Data Scientist with 6+ years
                of experience developing, deploying, and operating production
                ML systems. Expertise spanning deep learning, reinforcement
                learning, quantitative research, and LLM-based systems,
                with an emphasis on rigorous experimentation and
                end-to-end engineering ownership.
            </p>
        </div>
    </section>

	<div class="grid gap-6 lg:grid-cols-2">

		<!-- Education -->
		<section aria-labelledby="education">
			<div class="card h-full p-7">
				<h2 id="education" class="eyebrow">Education</h2>

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
		</section>

		<!-- Publications -->
		<section aria-labelledby="publications">
			<div class="card h-full p-7">
				<h2 id="publications" class="eyebrow">Publications</h2>

				<div class="mt-5">
					<div class="font-bold text-gray-950">
						Automated Well Status Identification in US Offshore
						Operations Using Machine Learning
					</div>

					<div class="mt-2 text-sm text-gray-500">
						SPE Offshore Europe · 2025 · Co-Author
					</div>

					<p class="mt-3 text-sm leading-6 text-gray-600">
						Developed XGBoost and 2D CNN models with engineered
						features to improve offshore well status classification
						accuracy.
					</p>

					<a
						href="https://doi.org/10.2118/226758-MS"
						target="_blank"
						rel="noopener noreferrer"
						class="mt-4 inline-flex items-center gap-2 rounded-md bg-gray-900 px-5 py-3 text-sm font-bold !text-white shadow-sm transition-colors hover:bg-gray-700"
					>
						View Publication <span aria-hidden="true">↗</span>
					</a>
				</div>
			</div>
		</section>

	</div>

    <!-- <section aria-labelledby="publications">
        <div class="card h-full p-7">
            <h2 id="publications" class="eyebrow">Publications</h2>

            <div class="mt-5">
                <div class="font-bold text-gray-950">
                    Automated Well Status Identification in US Offshore
                    Operations Using Machine Learning
                </div>

                <div class="mt-2 text-sm text-gray-500">
                    SPE Offshore Europe · 2025 · Co-Author
                </div>

                <p class="mt-3 text-sm leading-6 text-gray-600">
                    Developed XGBoost and 2D CNN models with engineered
                    features to improve offshore well status classification
                    accuracy.
                </p>

                <a
                    href="https://doi.org/10.2118/226758-MS"
                    target="_blank"
                    rel="noopener noreferrer"
                    class="mt-4 inline-flex items-center gap-2 rounded-md bg-gray-900 px-5 py-3 text-sm font-bold !text-white shadow-sm transition-colors hover:bg-gray-700"
                >
                    View Publication <span aria-hidden="true">↗</span>
                </a>
            </div>
        </div>
    </section> -->
</div>

	<section aria-labelledby="experience">
		<h2 id="experience" class="eyebrow mb-5">Experience</h2>
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

	<section aria-labelledby="skills">
		<div class="card p-7">
			<h2 id="skills" class="eyebrow">Technical Skills</h2>

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
	</section>

	<section aria-labelledby="education">
		<div class="card p-7">
			<h2 id="education" class="eyebrow">Education</h2>

			<div class="mt-5 space-y-6">
				<div>
					<div class="font-bold text-gray-950">M.S. Analytics · Computational Track</div>
					<div class="mt-1 text-sm text-gray-500">Georgia Institute of Technology · 2025</div>
				</div>

				<div>
					<div class="font-bold text-gray-950">B.S. Chemical & Biomolecular Engineering</div>
					<div class="mt-1 text-sm text-gray-500">University of Houston · 2017</div>
				</div>

				<div>
					<div class="font-bold text-gray-950">B.S. Biology · Minor in Psychology</div>
					<div class="mt-1 text-sm text-gray-500">Texas A&M University · 2014</div>
				</div>
			</div>
		</div>
	</section>

	<section aria-labelledby="publications">
		<div class="card p-7">
			<h2 id="publications" class="eyebrow">Publications</h2>

			<div class="mt-5">
				<div class="font-bold text-gray-950">
					Automated Well Status Identification in US Offshore Operations Using Machine Learning
				</div>

				<div class="mt-2 text-sm text-gray-500">SPE Offshore Europe · 2025 · Co-Author</div>

				<p class="mt-3 text-sm leading-6 text-gray-600">
					Developed XGBoost and 2D CNN models with engineered features to improve offshore well
					status classification accuracy.
				</p>

				<a
					href="https://doi.org/10.2118/226758-MS"
					target="_blank"
					rel="noopener noreferrer"
					class="mt-4 inline-flex items-center gap-2 rounded-md bg-gray-900 px-5 py-3 text-sm font-bold !text-white shadow-sm transition-colors hover:bg-gray-700"
				>
					View Publication <span aria-hidden="true">↗</span>
				</a>
			</div>
		</div>
	</section>
</div>
