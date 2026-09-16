<script lang="ts">
	import ProjectCard from '$lib/components/ProjectCard.svelte';
	import SectionHeader from '$lib/components/SectionHeader.svelte';
	import TechTag from '$lib/components/TechTag.svelte';
</script>

<svelte:head>
	<title>Ashley Taken | Machine Learning Engineer</title>

	<meta
		name="description"
		content="Machine learning engineering portfolio covering production ML, quantitative research, agentic AI, and full-stack technical systems."
	/>
</svelte:head>

<section class="border-b border-gray-200 bg-white">
    <div class="page-shell pt-8 pb-6 md:pt-10 md:pb-7">
		<div class="max-w-5xl">
			<div class="eyebrow mb-5">
				Machine Learning · Applied AI · Quantitative Research
			</div>

			<h1
				class="max-w-4xl text-4xl font-black tracking-tight text-gray-950 md:text-6xl md:leading-[1.05]"
			>
				Building rigorous ML systems from
				<span class="gradient-text"> research to production.</span>
			</h1>

			<p class="mt-3 max-w-3xl text-lg leading-8 text-gray-500">
				Machine learning engineer and data scientist specializing in production ML,
				time-series modeling, agentic AI, statistical experimentation, and full-stack
				technical systems.
			</p>

			<div class="mt-5 flex flex-wrap gap-2">
                <a
                    href="/experience"
                    class="rounded-md border border-purple-200 bg-purple-50 px-4 py-2.5 text-sm font-bold text-purple-800 transition hover:bg-purple-100"
                >
                    Experience
                </a>

				<a
					href="/contact"
					class="rounded-md border border-purple-200 bg-purple-50 px-4 py-2.5 text-sm font-bold text-purple-800 transition hover:bg-purple-100"
				>
					Contact
				</a>

                <a
                    href="/Ashley-Taken-Resume.pdf"
                    target="_blank"
                    rel="noopener noreferrer"
                    class="rounded-md border border-purple-200 bg-purple-50 px-4 py-2.5 text-sm font-bold text-purple-800 transition hover:bg-purple-100"
                >
                    Resume PDF
                </a>
			</div>
		</div>
	</div>
</section>

<section id="projects" class="page-shell pt-6 pb-16 md:pt-8 md:pb-20">
	<SectionHeader
		eyebrow="Featured Work"
		title="Selected engineering systems"
		description="Deep technical projects spanning quantitative research infrastructure, AI research systems, and production machine learning."
	/>

	<div class="grid gap-6 lg:grid-cols-3">
		<ProjectCard
			number="01"
			title="Quantitative ML Research Platform"
			subtitle="Taken Group LLC"
			description="A modular financial machine-learning research platform for dataset construction, statistical calibration, event-driven sampling, feature generation, experiment persistence, model research, and leakage-aware evaluation."
			href="/projects/quant-research"
			tags={['FastAPI', 'SvelteKit', 'Python', 'Docker', 'Time Series']}
			accent="purple"
		/>

		<div
			class="relative flex h-full flex-col rounded-2xl border border-gray-200 bg-white p-6 shadow-sm"
		>
			<div class="flex items-start justify-between gap-4">
				<div class="text-sm font-black text-blue-600">
					02
				</div>

				<div
					class="rounded-full border border-blue-200 bg-blue-50 px-3 py-1 text-[11px] font-bold uppercase tracking-wide text-blue-700"
				>
					Coming Soon
				</div>
			</div>

			<div class="mt-5">
				<div class="text-xs font-bold uppercase tracking-[0.16em] text-gray-400">
					Agentic Research Platform
				</div>

				<h3 class="mt-2 text-xl font-bold tracking-tight text-gray-950">
					AI Research & Codebase Intelligence
				</h3>

				<p class="mt-3 text-sm leading-6 text-gray-500">
					A quantitative research copilot combining codebase intelligence, literature
					retrieval, hybrid search, cross-encoder reranking, MCP tooling, task routing,
					and a dedicated evaluation framework.
				</p>
			</div>

			<div class="mt-auto flex flex-wrap gap-2 pt-6">
				{#each ['RAG', 'Agents', 'MCP', 'BM25', 'LLM Evaluation'] as tag}
					<TechTag label={tag} />
				{/each}
			</div>
		</div>

		<div
			class="relative flex h-full flex-col rounded-2xl border border-gray-200 bg-white p-6 shadow-sm"
		>
			<div class="flex items-start justify-between gap-4">
				<div class="text-sm font-black text-gray-700">
					03
				</div>

				<div
					class="rounded-full border border-gray-200 bg-gray-50 px-3 py-1 text-[11px] font-bold uppercase tracking-wide text-gray-600"
				>
					Coming Soon
				</div>
			</div>

			<div class="mt-5">
				<div class="text-xs font-bold uppercase tracking-[0.16em] text-gray-400">
					Energy & Engineering Systems
				</div>

				<h3 class="mt-2 text-xl font-bold tracking-tight text-gray-950">
					Production ML for Real Time Industrial Classification
				</h3>

				<p class="mt-3 text-sm leading-6 text-gray-500">
                    Designed and deployed a 2D CNN inference workflow in Dockerized Python services on Azure for real time industrial state classification, improving prediction accuracy from 77% to 98%. Proprietary implementation details and operational data are omitted.
				</p>
			</div>

			<div class="mt-auto flex flex-wrap gap-2 pt-6">
				{#each ['PyTorch', 'Azure', 'Docker', 'CNN', 'Model Monitoring'] as tag}
					<TechTag label={tag} />
				{/each}
			</div>
		</div>

		<!-- <ProjectCard
			number="02"
			title="AI Research & Codebase Intelligence"
			subtitle="Agentic Research Platform"
			description="A quantitative research copilot combining codebase intelligence, literature retrieval, hybrid search, cross-encoder reranking, MCP tooling, task routing, and a dedicated evaluation framework."
			href="/projects/research-agent"
			tags={['RAG', 'Agents', 'MCP', 'BM25', 'LLM Evaluation']}
			accent="blue"
		/>

		<ProjectCard
			number="03"
			title="Production ML & Industrial Analytics"
			subtitle="Energy & Engineering Systems"
			description="Production machine-learning inference, engineering applications, real-time operational analytics, and enterprise AI systems deployed across industrial workflows."
			href="/projects/production-ml"
			tags={['PyTorch', 'Azure', 'Docker', 'AVEVA PI', 'RAG']}
			accent="dark"
		/> -->
	</div>
</section>