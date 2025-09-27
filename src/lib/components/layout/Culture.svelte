<script lang="ts">
	import { animate, stagger } from "motion";
	import { onMount } from "svelte";
	import AnimateText from "$lib/components/animation/AnimateText.svelte";

	// Types
	export type Value = {
		title: string;
		description: string;
	};

	// Props
	const { values = [], ...rest }: { values: Value[]; [key: string]: any } = $props();

	let cards: HTMLElement[] = $state([]);

	onMount(() => {
		if (!cards.length) return;
		if (window.self !== window.top) return;

		animate(
			cards,
			{
				y: ["1.5rem", 0],
				filter: ["blur(2px)", "blur(0px)"],
				opacity: [0, 1]
			},
			{
				duration: 0.3,
				ease: "easeOut",
				delay: stagger(0.1, {
					ease: "easeInOut"
				})
			}
		);
	});
</script>

<section class="bg-gray-950 text-white" {...rest}>
	<div
		class="section-py section-px container mx-auto grid gap-12 [--gap:--spacing(8)] [--radius:var(--radius-2xl)]"
	>
		<div class="section-pb-sm container-sm grid text-balance text-title2">
			<h2 class="text-white">
				<AnimateText text="Five pillars of learning." />
			</h2>
			<p class="text-gray-300">
				<AnimateText text="The educational framework that transforms how students engage with knowledge and AI" />
			</p>
		</div>

		<div
			class="grid gap-8"
			style:grid-template-columns="repeat(auto-fit, minmax(320px, 1fr))"
		>
			{#each values as value, i}
				<div
					bind:this={cards[i]}
					class={[
						'relative bg-gray-900 rounded-xl p-6 border border-gray-800 hover:border-gray-700 transition-colors duration-200',
						i === 0 ? 'border-l-4 border-l-blue-500' : '',
						i === 1 ? 'border-l-4 border-l-orange-500' : '',
						i === 2 ? 'border-l-4 border-l-green-500' : '',
						i === 3 ? 'border-l-4 border-l-purple-500' : '',
						i === 4 ? 'border-l-4 border-l-yellow-500' : ''
					]}
				>
					<!-- Content -->
					<div class="space-y-4">
						<div class="text-title3 font-semibold text-white">{value.title}</div>
						<div class="text-body text-gray-300 leading-relaxed">{value.description}</div>
					</div>
				</div>
			{/each}
		</div>

		<!-- Additional insight section -->
		<div class="bg-gray-900 rounded-2xl p-8 border border-gray-800 mt-8">
			<div class="max-w-4xl">
				<h3 class="text-title2 text-white mb-4">The AURA approach</h3>
				<p class="text-headline text-gray-300 leading-relaxed">
					Our Five Pillars work together to create structured Social-Emotional Learning (AURA) that helps every student—especially bilingual learners, gifted minds, and builder-types—thrive in an environment where technology amplifies human potential rather than replacing it.
				</p>
			</div>
		</div>
	</div>
</section>
