<script lang="ts">
	import ArchitectureStep from '$lib/components/ArchitectureStep.svelte';
	import SectionHeader from '$lib/components/SectionHeader.svelte';
	import TechTag from '$lib/components/TechTag.svelte';

	const tags = [
		'FastAPI',
		'Open WebUI',
		'OpenRouter',
		'LangGraph',
		'ChromaDB',
		'BM25',
		'Cross-Encoder Reranking',
		'MCP',
		'Docker',
		'LLM Evaluation'
	];

	const modes = [
		{
			title: 'Codebase Analysis',
			body:
				'Retrieves implementation-specific context and identifies relevant files, modules, functions, and architecture touchpoints.'
		},
		{
			title: 'Literature Review',
			body:
				'Prioritizes research papers and technical references for paper-focused analysis and methodological comparison.'
		},
		{
			title: 'Cross-Source Synthesis',
			body:
				'Combines retrieved literature, code, and project context to connect research ideas to implementation decisions.'
		},
		{
			title: 'Critique',
			body:
				'Focuses on weaknesses, failure modes, leakage risks, methodological gaps, and missing evaluations.'
		},
		{
			title: 'Experiment Design',
			body:
				'Produces structured hypotheses, implementation touchpoints, validation plans, and evaluation metrics.'
		},
		{
			title: 'Research Guidance',
			body:
				'Supports broader research questions with evidence grounded across project documentation, literature, and code.'
		}
	];

	const evalMetrics = [
		['Retrieval', 'Recall@K · MRR'],
		['Answer Quality', 'Faithfulness · Usefulness'],
		['Research Quality', 'Experiment Quality · Insightfulness'],
		['Technical Depth', 'Code Understanding · Implementation Specificity'],
		['Synthesis', 'Cross-Source Synthesis · Paper Relevance'],
		['Routing', 'Task-Mode Match · Retrieval-Mode Match'],
		['Operations', 'P50 / P95 Retrieval and Agent Latency']
	];
</script>

<svelte:head>
	<title>AI Research & Codebase Intelligence | Ashley Taken</title>
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
			<div class="eyebrow">Taken Group LLC · Agentic AI Research Platform</div>

			<h1 class="mt-4 text-4xl font-black tracking-tight text-gray-950 md:text-5xl">
				AI Research & Codebase Intelligence
			</h1>

			<p class="mt-6 max-w-4xl text-lg leading-8 text-gray-500">
				A quantitative research copilot designed to reason across source code, technical
				literature, project documentation, and research context using hybrid retrieval,
				reranking, task-aware routing, tool access, and dedicated evaluation.
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
			<div class="metric-label">System Type</div>
			<div class="mt-2 font-bold text-gray-950">Research Copilot</div>
		</div>

		<div class="card p-5">
			<div class="metric-label">Knowledge Sources</div>
			<div class="mt-2 font-bold text-gray-950">Code + Literature + Docs</div>
		</div>

		<div class="card p-5">
			<div class="metric-label">Retrieval</div>
			<div class="mt-2 font-bold text-gray-950">Dense + BM25 + Reranking</div>
		</div>

		<div class="card p-5">
			<div class="metric-label">Evaluation</div>
			<div class="mt-2 font-bold text-gray-950">Retrieval + LLM Quality</div>
		</div>
	</div>
</section>

<section class="border-y border-gray-200 bg-white">
	<div class="page-shell py-16">
		<SectionHeader
			eyebrow="Platform Overview"
			title="Research, retrieval, tooling, and evaluation in one workflow"
			description="The platform combines a conversational research interface with codebase search, literature retrieval, tool use, and measurable evaluation."
		/>

		<div class="grid gap-6 lg:grid-cols-2">
			<div class="card flex min-h-[320px] items-center justify-center bg-gray-50">
				<div class="text-center">
					<div class="metric-label">Screenshot Placeholder</div>
					<div class="mt-2 font-bold text-gray-700">
						Research Agent Interface
					</div>
				</div>
			</div>

			<div class="card flex min-h-[320px] items-center justify-center bg-gray-50">
				<div class="text-center">
					<div class="metric-label">Screenshot Placeholder</div>
					<div class="mt-2 font-bold text-gray-700">
						Evaluation Dashboard
					</div>
				</div>
			</div>
		</div>
	</div>
</section>

<section class="page-shell py-16">
	<SectionHeader
		eyebrow="System Architecture"
		title="A research pipeline built around evidence and evaluation"
	/>

	<div class="grid gap-4 md:grid-cols-2 xl:grid-cols-5">
		<ArchitectureStep
			number="01"
			title="User Interface"
			description="Open WebUI provides model selection, custom agents, and tool access."
			accent="blue"
		/>

		<ArchitectureStep
			number="02"
			title="Task Routing"
			description="Questions are classified by research mode before retrieval."
			accent="blue"
		/>

		<ArchitectureStep
			number="03"
			title="Hybrid Retrieval"
			description="Dense search, BM25, metadata, and reranking assemble context."
			accent="blue"
		/>

		<ArchitectureStep
			number="04"
			title="Tools & MCP"
			description="The agent can access project tools and code-aware interfaces."
			accent="blue"
		/>

		<ArchitectureStep
			number="05"
			title="Evaluation"
			description="Retrieval and response quality are tracked across comparable runs."
			accent="blue"
		/>
	</div>
</section>

<section class="page-shell py-16">
	<SectionHeader
		eyebrow="Task Routing"
		title="Different research questions require different retrieval behavior"
		description="Rather than forcing every question through one generic RAG path, the agent classifies tasks and adjusts retrieval scope, weighting, and response style."
	/>

	<div class="grid gap-5 md:grid-cols-2 xl:grid-cols-3">
		{#each modes as mode}
			<div class="card p-6">
				<h3 class="font-bold text-gray-950">{mode.title}</h3>
				<p class="mt-3 text-sm leading-6 text-gray-500">{mode.body}</p>
			</div>
		{/each}
	</div>
</section>

<section class="border-y border-gray-200 bg-white">
	<div class="page-shell py-16">
		<div class="grid gap-10 lg:grid-cols-[0.9fr_1.1fr]">
			<div>
				<SectionHeader
					eyebrow="Knowledge Pipeline"
					title="Continuous codebase intelligence"
					description="The system maintains an evolving searchable representation of the active codebase and supporting research materials."
				/>

				<p class="text-sm leading-6 text-gray-500">
					A filesystem watcher detects create, modify, move, and delete events. Changed
					files are selectively reprocessed so the research agent can reason against a
					current view of the implementation without requiring a full manual re-index.
				</p>

				<p class="mt-4 text-sm leading-6 text-gray-500">
					Technical documents and research papers follow a parallel ingestion path with
					content extraction, chunking, metadata enrichment, embedding generation, and
					search indexing.
				</p>
			</div>

			<div class="card overflow-hidden">
				<div class="divide-y divide-gray-200">
					{#each [
						['01', 'File or document changes'],
						['02', 'Content extraction and metadata enrichment'],
						['03', 'Chunking and embedding'],
						['04', 'Dense and lexical indexing'],
						['05', 'Searchable agent context']
					] as step}
						<div class="flex gap-5 p-5">
							<div class="metric-label w-8 shrink-0">{step[0]}</div>
							<div class="text-sm font-bold text-gray-950">{step[1]}</div>
						</div>
					{/each}
				</div>
			</div>
		</div>
	</div>
</section>

<section class="page-shell py-16">
	<SectionHeader
		eyebrow="Evaluation"
		title="Agent quality is measured, not assumed"
		description="A dedicated evaluation harness separates retrieval performance from answer quality and records comparable run-level and case-level results."
	/>

	<div class="grid gap-5 lg:grid-cols-[1fr_1fr]">
		<div class="card p-7">
			<h3 class="text-lg font-bold text-gray-950">Evaluation Dimensions</h3>

			<div class="mt-5 divide-y divide-gray-200">
				{#each evalMetrics as metric}
					<div class="grid gap-1 py-4 sm:grid-cols-[160px_1fr]">
						<div class="text-sm font-bold text-gray-900">{metric[0]}</div>
						<div class="text-sm text-gray-500">{metric[1]}</div>
					</div>
				{/each}
			</div>
		</div>

		<div class="card bg-gray-950 p-7 text-white">
			<div class="metric-label !text-gray-400">Evaluation Flow</div>

			<div class="mt-6 space-y-3 text-sm">
				<div class="rounded-md border border-gray-700 bg-gray-900 p-4">
					Curated Evaluation Set
				</div>
				<div class="text-center text-gray-500">↓</div>
				<div class="rounded-md border border-gray-700 bg-gray-900 p-4">
					Retrieval Run + Agent Response
				</div>
				<div class="text-center text-gray-500">↓</div>
				<div class="rounded-md border border-gray-700 bg-gray-900 p-4">
					Recall / MRR / Routing Checks
				</div>
				<div class="text-center text-gray-500">↓</div>
				<div class="rounded-md border border-gray-700 bg-gray-900 p-4">
					Structured Quality Scoring + LLM Judge
				</div>
				<div class="text-center text-gray-500">↓</div>
				<div class="rounded-md border border-blue-700 bg-blue-950/40 p-4">
					Run History · Trends · A/B Comparison · Per-Case Inspection
				</div>
			</div>
		</div>
	</div>
</section>

<section class="border-y border-gray-200 bg-white">
	<div class="page-shell py-16">
		<SectionHeader
			eyebrow="Evaluation Design"
			title="Tests cover multiple research competencies"
			description="Evaluation sets are structured around the actual jobs the research assistant is expected to perform rather than generic chatbot questions."
		/>

		<div class="grid gap-4 md:grid-cols-2 lg:grid-cols-5">
			{#each [
				['Codebase', 'Implementation-aware technical analysis'],
				['Literature', 'Paper-focused reasoning and comparison'],
				['Synthesis', 'Connecting research ideas to code'],
				['Critique', 'Identifying weaknesses and failure modes'],
				['Experiment', 'Designing concrete validation plans']
			] as item}
				<div class="card p-5">
					<div class="text-sm font-bold text-gray-950">{item[0]}</div>
					<div class="mt-2 text-xs leading-5 text-gray-500">{item[1]}</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<section class="page-shell py-16">
	<div class="grid gap-8 lg:grid-cols-2">
		<div class="card p-7">
			<div class="eyebrow">Infrastructure</div>

			<h2 class="mt-3 text-2xl font-bold text-gray-950">
				Containerized multi-service architecture
			</h2>

			<p class="mt-4 text-sm leading-6 text-gray-500">
				The application is deployed as cooperating Docker services separating the user
				interface, research-agent API, reranker, MCP proxy, document processing, and supporting
				services.
			</p>

			<div class="mt-6 grid gap-3 sm:grid-cols-2">
				{#each [
					'Open WebUI',
					'Agent API',
					'Cross-Encoder Reranker',
					'MCP Proxy',
					'Document Extraction',
					'Persistent Vector Store'
				] as service}
					<div class="rounded-md border border-gray-200 bg-gray-50 p-3 text-sm font-semibold">
						{service}
					</div>
				{/each}
			</div>
		</div>

		<div class="card p-7">
			<div class="eyebrow">Model Layer</div>

			<h2 class="mt-3 text-2xl font-bold text-gray-950">
				Model-agnostic inference
			</h2>

			<p class="mt-4 text-sm leading-6 text-gray-500">
				The research platform is not tied to a single model provider. OpenRouter-backed model
				selection makes it possible to compare different frontier models while keeping the
				retrieval, tooling, and evaluation infrastructure consistent.
			</p>

			<div class="mt-6 rounded-md border border-purple-200 bg-purple-50 p-4">
				<div class="text-sm font-bold text-purple-900">
					Stable research infrastructure, interchangeable model layer
				</div>
			</div>
		</div>
	</div>
</section>

<section class="border-t border-gray-200 bg-white">
	<div class="page-shell py-12">
		<div class="text-sm text-gray-500">
			Public portfolio materials use sanitized examples. Private prompts, proprietary research
			direction, internal knowledge sources, credentials, and sensitive tool configuration are
			intentionally omitted.
		</div>
	</div>
</section>