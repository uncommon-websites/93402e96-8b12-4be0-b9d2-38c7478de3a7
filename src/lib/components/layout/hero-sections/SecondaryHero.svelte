<script lang="ts">
	import AnimateText from "$lib/components/animation/AnimateText.svelte";

	let {
		title,
		subtitle,
		imageSrc = "https://www.unc.mn/image-placeholder.svg",
		...rest
	}: {
		title: string;
		subtitle: string;
		imageSrc: string;
		[key: string]: any;
	} = $props();
</script>

<header class="relative overflow-hidden bg-gradient-to-br from-background via-background to-muted/20" {...rest}>
	<div class="section-px section-py container mx-auto">
		<div class="grid gap-12 lg:grid-cols-2 lg:gap-16 xl:gap-20 items-center">
			<!-- Content Column -->
			<div class="space-y-8">
				<div class="space-y-6">
					<h1 class="text-display font-[450] tracking-tight text-balance leading-[1.1]">
						<AnimateText text={title} />
					</h1>
					<p class="text-title3 text-muted-foreground font-normal leading-relaxed">
						<AnimateText text={subtitle} />
					</p>
				</div>
				
				<!-- Mission statement -->
				<div class="prose prose-lg max-w-none">
					<p class="text-body text-foreground/80 leading-relaxed">
						We exist because the future demands something different. In a world where AI reshapes how we think and work, students need more than traditional education—they need to learn how to lead with technology, not follow it.
					</p>
				</div>

				<!-- Key principles -->
				<div class="grid gap-4 sm:grid-cols-2">
					<div class="space-y-2">
						<div class="text-headline font-medium text-foreground">Human-centered</div>
						<p class="text-caption text-muted-foreground">Teachers lead, technology amplifies</p>
					</div>
					<div class="space-y-2">
						<div class="text-headline font-medium text-foreground">Process-focused</div>
						<p class="text-caption text-muted-foreground">How you think matters more than what you produce</p>
					</div>
					<div class="space-y-2">
						<div class="text-headline font-medium text-foreground">Mission-driven</div>
						<p class="text-caption text-muted-foreground">Real projects with real impact</p>
					</div>
					<div class="space-y-2">
						<div class="text-headline font-medium text-foreground">Future-ready</div>
						<p class="text-caption text-muted-foreground">AI-literate graduates prepared for tomorrow</p>
					</div>
				</div>
			</div>

			<!-- Image Column -->
			<div class="relative">
				<div class="aspect-[4/3] overflow-hidden rounded-2xl bg-muted">
					<img
						class="h-full w-full object-cover transition-transform duration-700 hover:scale-105"
						src={imageSrc}
						alt="Students collaborating on innovative projects in our Vienna learning environment"
					/>
				</div>
				
				<!-- Decorative accent -->
				<div class="absolute -top-4 -right-4 w-24 h-24 bg-primary/10 rounded-full blur-xl"></div>
				<div class="absolute -bottom-8 -left-8 w-32 h-32 bg-secondary/5 rounded-full blur-2xl"></div>
			</div>
		</div>
	</div>
</header>
