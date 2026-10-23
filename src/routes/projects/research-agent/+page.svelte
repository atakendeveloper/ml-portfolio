<script lang="ts">
	import SectionHeader from '$lib/components/SectionHeader.svelte';
	import TechTag from '$lib/components/TechTag.svelte';

	const tags = [
		'Python',
		'FastAPI',
		'Open WebUI',
		'LangGraph',
		'ChromaDB',
		'BM25',
		'Cross Encoder Reranking',
		'MCP',
		'Docker',
		'LLM Evaluation'
	];
	const modes = [
		['Codebase Analysis', 'Find relevant files and explain implementation behavior.'],
		['Literature Review', 'Retrieve technical papers and compare research methods.'],
		['Research Synthesis', 'Connect ideas from literature to implementation decisions.'],
		['Critique', 'Identify weaknesses and propose tests for missing evidence.'],
		['Experiment Design', 'Draft hypotheses with ablations and validation plans.'],
		['Research Guidance', 'Explore research directions using code and document context.']
	];
	const metrics = [
		['Retrieval', 'MRR · Recall@K'],
		['Answer Quality', 'Usefulness · Source-grounded faithfulness'],
		['Research Quality', 'Experiment quality · Insightfulness · Synthesis'],
		['Technical Depth', 'Code understanding · Implementation specificity'],
		['Routing', 'Task mode match · Retrieval mode match'],
		['Operations', 'P50 / P95 retrieval and agent latency']
	];

	const demonstrations = [
		{
			title: 'Research Agent',
			description: 'Interactive research workspace for technical literature and codebase analysis.',
			images: [
				{
					src: '/images/agent/agent-workspace.png',
					alt: 'Research workspace with model selection and research controls.',
					caption: 'Research workspace with OpenRouter model selection and configurable research modes.'
				},
				{
					src: '/images/agent/agent-research-output.png',
					alt: 'Research agent generating a structured experiment proposal.',
					caption: 'Example of a structured research and experiment proposal. Prior conversations and indexed research materials omitted for publication.'
				}
			]
		},
		{
			title: 'Evaluation Dashboard',
			description: 'Evaluation tools for analyzing retrieval and research-agent performance.',
			images: [
				{
					src: '/images/agent/eval-overview.png',
					alt: 'Evaluation dashboard showing research-agent performance metrics.',
					caption: 'Evaluation dashboard for saved runs and performance metrics.'
				},
				{
					src: '/images/agent/eval-results.png',
					alt: 'Detailed evaluation results for retrieval and agent responses.',
					caption: 'Detailed evaluation results and case-level inspection.'
				}
			]
		}
	];
</script>

<svelte:head>
	<title>AI Research &amp; Codebase Intelligence | Ashley Taken</title>
	<meta
		name="description"
		content="A quantitative ML research copilot built with LangGraph and hybrid retrieval. Explore its architecture and evaluation workflow."
	/>
</svelte:head>

<section class="border-b border-gray-200 bg-white">
	<div class="page-shell py-10 md:py-12">
		<a
			href="/#projects"
			class="mb-4 inline-flex text-sm font-semibold text-gray-500 hover:text-gray-950"
			>← Back to projects</a
		>
		<div class="max-w-5xl">
			<div class="eyebrow">Taken Group LLC · Agentic Research Platform</div>
			<h1 class="mt-3 text-4xl font-black tracking-tight text-gray-950 md:text-5xl">
				AI Research &amp; Codebase Intelligence
			</h1>
			<p class="mt-4 max-w-4xl text-lg leading-8 text-gray-500">
				A quantitative ML research copilot that connects technical literature to source code. Hybrid
				retrieval and a staged LangGraph workflow support research analysis and experiment proposals
				with a dedicated evaluation harness.
			</p>
			<div class="mt-5 flex flex-wrap gap-2">
				{#each tags as tag}<TechTag label={tag} />{/each}
			</div>
		</div>
	</div>
</section>

<section class="bg-white">
	<div class="page-shell py-10 md:py-12">
		<SectionHeader
			eyebrow="Architecture"
			title="From source documents to research decisions"
			description="Knowledge ingestion and retrieval support the agent workflow. Evaluation runs inspect retrieval behavior and response quality separately."
		/>
		<figure class="card overflow-hidden p-2">
			<a
				href="/images/research-agent/architecture-overview.svg"
				target="_blank"
				rel="noopener noreferrer"
				class="block cursor-zoom-in rounded-lg focus-visible:outline-2 focus-visible:outline-blue-600"
				aria-label="Open research agent architecture diagram at full size in a new tab"
			>
				<img
					src="/images/research-agent/architecture-overview.svg"
					alt="Four architecture layers: source documents feed knowledge ingestion and retrieval. LangGraph orchestrates research responses. Evaluation compares saved runs and research proposals."
					width="1800"
					height="1050"
					class="h-auto w-full"
				/>
			</a>
			<figcaption class="px-3 py-3 text-xs leading-5 text-gray-500">
				Open the diagram to examine full size. Dashed connections show optional cross encoder
				reranking and configured MCP tool access.
			</figcaption>
		</figure>
	</div>
</section>

<section class="border-y border-gray-200 bg-gray-50">
	<div class="page-shell grid gap-5 py-10 md:py-12 md:grid-cols-2 xl:grid-cols-4">
		<div class="card p-6">
			<div class="eyebrow">Knowledge &amp; Retrieval</div>
			<h2 class="mt-3 text-xl font-bold text-gray-950">Context across code and literature</h2>
			<p class="mt-3 text-sm leading-6 text-gray-500">
				Document extraction and metadata enrichment feed SentenceTransformers embeddings in ChromaDB
				and a BM25 index. Hybrid search combines dense and lexical rankings through reciprocal rank
				fusion with corpus weighting and source diversification.
			</p>
			<p class="mt-3 text-sm leading-6 text-gray-500">
				A filesystem watcher tracks changes. Content hashes and embedding version checks support
				selective reindexing.
			</p>
			<p class="mt-3 text-sm leading-6 text-gray-500">
				Optional cross encoder reranking is available through the dense search API. The core graph
				uses dense or hybrid retrieval.
			</p>
		</div>
		<div class="card p-6">
			<div class="eyebrow">Agent Orchestration</div>
			<h2 class="mt-3 text-xl font-bold text-gray-950">A staged research workflow</h2>
			<p class="mt-3 text-sm leading-6 text-gray-500">
				Heuristic task routing selects a research mode and adjusts retrieval scope and corpus
				weights. LangGraph runs retrieval then planning and research synthesis. An optional
				implementation mapping stage precedes final review.
			</p>
			<p class="mt-3 text-sm leading-6 text-gray-500">
				Configured MCP tools can supply context before planning. Responses request evidence
				references and structured recommendations or experiment proposals.
			</p>
		</div>
		<div class="card p-6">
			<div class="eyebrow">Engineering</div>
			<h2 class="mt-3 text-xl font-bold text-gray-950">Modular services and model access</h2>
			<p class="mt-3 text-sm leading-6 text-gray-500">
				Open WebUI provides the conversational interface. FastAPI exposes agent and evaluation
				endpoints. Docker Compose connects the agent API with document processing and separate
				reranker and MCP proxy services.
			</p>
			<p class="mt-3 text-sm leading-6 text-gray-500">
				OpenAI compatible inference supports configurable models through OpenAI or OpenRouter while
				retaining the retrieval and evaluation infrastructure.
			</p>
		</div>
		<div class="card p-6">
			<div class="eyebrow">Evaluation Framework</div>
			<h2 class="mt-3 text-xl font-bold text-gray-950">
				Research quality and retrieval diagnostics
			</h2>

			<p class="mt-3 text-sm leading-6 text-gray-500">
				A dedicated evaluation harness runs curated test cases against retrieval
				and agent workflows. Metrics track retrieval relevance, response quality,
				research synthesis, and execution latency.
			</p>

			<p class="mt-3 text-sm leading-6 text-gray-500">
				Saved evaluation runs support performance comparisons, case-level inspection,
				and experiment notes.
			</p>
		</div>
	</div>
</section>


<section class="page-shell py-10 md:py-12">
	<SectionHeader
		eyebrow="Demonstration"
		title="Research interface and evaluation workspace"
		description="A look inside the research agent and its dedicated evaluation framework."
	/>

	<div class="grid gap-8 lg:grid-cols-2">
		{#each demonstrations as demo}
			<div class="card p-5">
				<h3 class="text-xl font-bold text-gray-950">
					{demo.title}
				</h3>

				<p class="mt-2 text-sm leading-6 text-gray-500">
					{demo.description}
				</p>

				<div class="mt-5 space-y-6">
					{#each demo.images as image}
						<figure>
							<a
								href={image.src}
								target="_blank"
								rel="noopener noreferrer"
								class="block overflow-hidden rounded-lg border border-gray-200"
							>
								<img
									src={image.src}
									alt={image.alt}
									loading="lazy"
									class="h-auto w-full transition-transform duration-200 hover:scale-[1.01]"
								/>
							</a>

							<figcaption class="mt-2 text-xs leading-5 text-gray-500">
								{image.caption}
							</figcaption>
						</figure>
					{/each}
				</div>
			</div>
		{/each}
	</div>

	<p class="mt-5 text-xs italic text-gray-400">
		Conversation history and selected project details omitted for publication.
	</p>
</section>

<section class="border-t border-gray-200 bg-white">
	<div class="page-shell py-8">
		<p class="text-xs leading-5 text-gray-500">
			Architecture is simplified for public presentation. Private research materials and sensitive
			configuration are omitted.
		</p>
	</div>
</section>
