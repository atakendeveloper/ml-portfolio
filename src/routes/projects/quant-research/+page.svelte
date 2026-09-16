<script lang="ts">
    import SectionHeader from '$lib/components/SectionHeader.svelte';
    import TechTag from '$lib/components/TechTag.svelte';

    const tags = [
        'Python',
        'FastAPI',
        'SvelteKit',
        'MariaDB',
        'Redis',
        'Docker',
        'PyTorch',
        'XGBoost',
        'Transformers',
        'Optuna',
        'Time Series',
        'Statistical Analysis'
    ];

    let architectureOpen = $state(false);
    let representationOpen = $state(false);
</script>

<svelte:head>
    <title>Quantitative ML Research Platform | Ashley Taken</title>
</svelte:head>

<section class="border-b border-gray-200 bg-white">
    <div class="page-shell py-10 md:py-12">
        <a
            href="/#projects"
            class="mb-4 inline-flex text-sm font-semibold text-gray-500 hover:text-gray-950"
        >
            ← Back to projects
        </a>

        <div class="max-w-5xl">
            <div class="eyebrow">Taken Group LLC · Founder / Machine Learning Engineer</div>

            <h1 class="mt-3 text-4xl font-black tracking-tight text-gray-950 md:text-5xl">
                Quantitative ML Research Platform
            </h1>

            <p class="mt-4 max-w-4xl text-lg leading-8 text-gray-500">
                A full-stack research environment for constructing financial datasets, running
                reproducible statistical studies, engineering features, evaluating event-sampling
                methods, training predictive models, and validating research decisions before live
                deployment.
            </p>

            <div class="mt-5 flex flex-wrap gap-2">
                {#each tags as tag}
                    <TechTag label={tag} />
                {/each}
            </div>
        </div>
    </div>
</section>

<section class="bg-white">
    <div class="page-shell py-10 md:py-12">
        <div class="eyebrow">
            Architecture
        </div>

        <div class="mt-4">
            <div class="mb-3 text-xs font-medium text-gray-400">
                Click the diagram to examine full size.
            </div>

            <button
                type="button"
                onclick={() => (architectureOpen = true)}
                class="group block w-full cursor-zoom-in overflow-hidden rounded-2xl border border-gray-200 bg-white p-2 text-left shadow-sm transition hover:border-purple-300 hover:shadow-md"
                aria-label="Open architecture diagram at full size"
            >
                <img
                    src="/images/quant/architecture-overview.svg"
                    alt="Architecture diagram for the quantitative ML research platform"
                    class="h-auto w-full"
                />
            </button>
        </div>

        {#if architectureOpen}
            <div class="fixed inset-0 z-50 flex items-center justify-center p-4 sm:p-8">
                <button
                    type="button"
                    class="absolute inset-0 cursor-zoom-out bg-gray-950/80 backdrop-blur-sm"
                    onclick={() => (architectureOpen = false)}
                    aria-label="Close architecture diagram"
                ></button>

                <div
                    class="relative z-10 flex max-h-[94vh] w-full max-w-[1750px] flex-col overflow-hidden rounded-2xl border border-gray-700 bg-white shadow-2xl"
                >
                    <div class="flex items-center justify-between border-b border-gray-200 px-5 py-3">
                        <div>
                            <div class="text-sm font-bold text-gray-950">
                                Quantitative ML Research Platform Architecture
                            </div>
                            <div class="text-xs text-gray-500">
                                Simplified for Public Portfolio — proprietary implementation details are intentionally omitted.
                            </div>
                        </div>

                        <button
                            type="button"
                            onclick={() => (architectureOpen = false)}
                            class="rounded-md border border-gray-300 bg-white px-3 py-1.5 text-sm font-bold text-gray-700 transition hover:bg-gray-100"
                        >
                            Close
                        </button>
                    </div>

                    <div class="overflow-auto bg-gray-100 p-4">
                        <img
                            src="/images/quant/architecture-overview.svg"
                            alt="Full-size architecture diagram for the quantitative ML research platform"
                            class="mx-auto h-auto min-w-[1400px] max-w-none"
                        />
                    </div>
                </div>
            </div>
        {/if}
    </div>
</section>

<section class="border-y border-gray-200 bg-gray-50">
    <div class="page-shell py-10 md:py-12">
        <SectionHeader
            eyebrow="Research Workflow"
            title="From market data to model-ready datasets"
            description="A reproducible research workflow for testing dataset construction, sampling methodology, stationarity, structural events, and feature behavior before modeling."
        />

        <div class="grid gap-6 lg:grid-cols-[1.5fr_0.5fr]">
            <div class="overflow-hidden rounded-2xl border border-gray-200 bg-white shadow-sm">
                <video
                    controls
                    muted
                    playsinline
                    preload="metadata"
                    class="aspect-video w-full bg-gray-950 object-contain"
                >
                    <source src="/videos/quant/research-pipeline.mp4" type="video/mp4" />
                </video>

                <div class="border-t border-gray-200 px-5 py-4">
                    <div class="text-sm font-bold text-gray-950">
                        Research & Statistical Pipeline
                    </div>

                    <p class="mt-1 text-sm leading-6 text-gray-500">
                        Public demo of dataset research, event studies, feature engineering, and
                        AI-assisted analysis. Proprietary parameter values and research conclusions
                        are intentionally redacted.
                    </p>
                </div>
            </div>

            <div class="grid gap-3">
                <div class="card p-5">
                    <div class="metric-label">Dataset Research</div>

                    <div class="mt-2 font-bold text-gray-950">
                        Exploration and sampling studies
                    </div>

                    <p class="mt-2 text-sm leading-6 text-gray-500">
                        Explore source data, compare alternative sampling approaches, and evaluate
                        stability, dependence, volatility, and distribution behavior.
                    </p>
                </div>

                <div class="card p-5">
                    <div class="metric-label">Event Research</div>

                    <div class="mt-2 font-bold text-gray-950">
                        Structural event selection
                    </div>

                    <p class="mt-2 text-sm leading-6 text-gray-500">
                        Evaluate multiple event-detection approaches using controlled comparisons,
                        overlap analysis, and stability diagnostics.
                    </p>
                </div>

                <div class="card p-5">
                    <div class="metric-label">Feature Engineering</div>

                    <div class="mt-2 font-bold text-gray-950">
                        Model-ready feature datasets
                    </div>

                    <p class="mt-2 text-sm leading-6 text-gray-500">
                        Combine validated statistical, technical, and event-derived features into
                        reproducible datasets with lineage and completeness diagnostics.
                    </p>
                </div>

                <div class="card p-5">
                    <div class="metric-label">Agentic Analysis</div>

                    <div class="mt-2 font-bold text-gray-950">
                        AI-assisted study interpretation
                    </div>

                    <p class="mt-2 text-sm leading-6 text-gray-500">
                        Generate and persist structured research summaries from completed studies,
                        with saved analysis history and reusable experiment context.
                    </p>
                </div>
            </div>
        </div>
    </div>
</section>

<section class="bg-white">
    <div class="page-shell py-10 md:py-12">
        <SectionHeader
            eyebrow="Model Research & Evaluation"
            title="From representation learning to out-of-sample validation"
            description="A complete modeling workflow for configuring experiments, training transformer representations, diagnosing model behavior, and evaluating performance out of sample."
        />

        <div class="grid gap-6 lg:grid-cols-[1.5fr_0.5fr]">
            <div class="overflow-hidden rounded-2xl border border-gray-200 bg-white shadow-sm">
                <video
                    controls
                    muted
                    playsinline
                    preload="metadata"
                    poster="/images/quant/model-training-poster.png"
                    class="aspect-video w-full bg-gray-950 object-contain"
                >
                    <source src="/videos/quant/model-training-evaluation.mp4" type="video/mp4" />
                </video>

                <div class="border-t border-gray-200 px-5 py-4">
                    <div class="text-sm font-bold text-gray-950">
                        Model Training & Evaluation
                    </div>

                    <p class="mt-2 text-xs leading-5 text-gray-400">
                        Portfolio demo run — metrics shown are from a non production experiment
                        created specifically to demonstrate the research workflow.
                    </p>
                </div>
            </div>
            <div>
                <div class="mb-3 text-xs font-medium text-gray-400">
                    Click diagram to examine full-size model design
                </div>

                <button
                    type="button"
                    onclick={() => (representationOpen = true)}
                    class="group block w-full cursor-zoom-in overflow-hidden rounded-2xl border border-gray-200 bg-white p-3 text-left shadow-sm transition hover:border-purple-300 hover:shadow-md"
                    aria-label="Open representation learning diagram at full size"
                >
                    <img
                        src="/images/quant/representation-learning-flow.svg"
                        alt="High-level representation learning model design"
                        class="h-auto w-full"
                    />
                </button>
            </div>
        </div>

        {#if representationOpen}
            <div class="fixed inset-0 z-50 flex items-center justify-center p-4 sm:p-8">
                <button
                    type="button"
                    class="absolute inset-0 cursor-zoom-out bg-gray-950/80 backdrop-blur-sm"
                    onclick={() => (representationOpen = false)}
                    aria-label="Close representation learning diagram"
                ></button>

                <div
                    class="relative z-10 flex max-h-[94vh] w-full max-w-[900px] flex-col overflow-hidden rounded-2xl border border-gray-700 bg-white shadow-2xl"
                >
                    <div class="flex items-center justify-between border-b border-gray-200 px-5 py-3">
                        <div>
                            <div class="text-sm font-bold text-gray-950">
                                Representation Learning (SNCC Model) Design
                            </div>

                            <div class="text-xs text-gray-500">
                                High-level self-supervised learning architecture
                            </div>
                        </div>

                        <button
                            type="button"
                            onclick={() => (representationOpen = false)}
                            class="rounded-md border border-gray-300 bg-white px-3 py-1.5 text-sm font-bold text-gray-700 transition hover:bg-gray-100"
                        >
                            Close
                        </button>
                    </div>

                    <div class="overflow-auto bg-gray-100 p-6">
                        <img
                            src="/images/quant/representation-learning-flow.svg"
                            alt="Full-size representation learning model design"
                            class="mx-auto h-auto w-full max-w-[700px]"
                        />
                    </div>
                </div>
            </div>
        {/if}
    </div>
</section>

<section class="border-y border-gray-200 bg-gray-50">
    <div class="page-shell py-10 md:py-12">
        <SectionHeader
            eyebrow="Platform Engineering"
            title="Research infrastructure built for reproducibility"
            description="The platform persists data, experiments, and intermediate artifacts so research can be reopened, compared, and reproduced instead of existing only inside one off notebooks."
        />

            <div class="grid gap-4 sm:grid-cols-2 xl:grid-cols-4">
                <div class="card p-5">
                    <div class="metric-label">Cache Architecture</div>

                    <div class="mt-2 font-bold text-gray-950">
                        Deterministic artifact layers
                    </div>

                    <p class="mt-2 text-sm leading-6 text-gray-500">
                        Dedicated cache layers persist bar construction, continuous-series data,
                        event studies, feature datasets, and downstream research artifacts.
                    </p>
                </div>

                <div class="card p-5">
                    <div class="metric-label">Execution</div>

                    <div class="mt-2 font-bold text-gray-950">
                        Background research jobs
                    </div>

                    <p class="mt-2 text-sm leading-6 text-gray-500">
                        Long-running studies and dataset builds execute outside the request lifecycle
                        while job state and completed results remain available to the UI.
                    </p>
                </div>

                <div class="card p-5">
                    <div class="metric-label">Lineage & Persistence</div>

                    <div class="mt-2 font-bold text-gray-950">
                        Reopenable research artifacts
                    </div>

                    <p class="mt-2 text-sm leading-6 text-gray-500">
                        Configurations, metadata, study history, and artifact identities are retained
                        so downstream datasets can be traced back to their research inputs.
                    </p>
                </div>

                <div class="card p-5">
                    <div class="metric-label">Application Services</div>

                    <div class="mt-2 font-bold text-gray-950">
                        FastAPI + SvelteKit + Docker
                    </div>

                    <p class="mt-2 text-sm leading-6 text-gray-500">
                        Python research services are exposed through API-backed application workflows
                        rather than isolated notebooks, with containerized supporting services.
                    </p>
                </div>
            </div>

        <div class="mt-8">
            <div class="eyebrow">
                Backend Repository Sample
            </div>

            <div class="mt-4 inline-block rounded-2xl border border-gray-200 bg-white p-3 shadow-sm">
                <img
                    src="/images/quant/backend-repo-structure.png"
                    alt="Selected backend repository structure for the quantitative ML research platform"
                    class="h-auto w-[300px] max-w-full"
                />
            </div>
        </div>
    </div>
</section>

<section class="border-t border-gray-200 bg-white">
    <div class="page-shell py-8">
        <div class="text-sm text-gray-500">
            Selected implementation details, proprietary strategy logic, and research conclusions are
            intentionally omitted.
        </div>
    </div>
</section>