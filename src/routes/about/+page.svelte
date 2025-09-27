<script lang="ts">
	// Components
	import CallToAction from "$lib/components/layout/CallToAction.svelte";

	// Icons
	import StakeholderGrid from "$lib/components/layout/StakeholderGrid.svelte";
	import Story from "./Story.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";

	// Constants
	const values = [
		{
			title: "Human-led learning",
			description: "Technology amplifies great teaching rather than replacing it."
		},
		{
			title: "Process over product",
			description: "How students think and iterate matters more than perfect final outcomes."
		},
		{
			title: "Real-world missions",
			description: "Students tackle authentic challenges that create genuine impact."
		},
		{
			title: "Ethical AI literacy",
			description: "Understanding both the power and responsibility that comes with AI tools."
		},
		{
			title: "Systems thinking",
			description: "Seeing connections, understanding complexity, and designing thoughtful solutions."
		}
	];
</script>

<SecondaryHero
	title="Where great minds build"
	subtitle="Human-led, AI-literate learning"
	imageSrc="/generated/image-a-small-group-of-diverse-students-and-a-.webp"
/>

<!-- Story Section -->
<Story
	paragraphs={[
		"We founded our school with a clear conviction: education must evolve as dramatically as the world around us. While others debate whether AI belongs in classrooms, we're pioneering how humans and AI can collaborate to unlock extraordinary learning.",
		"Our Vienna campus represents more than progressive education—it's a laboratory for the future. Here, internationally-minded families find an environment where academic rigor meets authentic AI literacy, where students don't just consume information but create solutions.",
		"From day one, we've asked ourselves: 'How do we prepare minds for a world that doesn't exist yet?' This question drives every curriculum decision, every teaching methodology, and every real-world mission we undertake with our students.",
		"We believe the future belongs to those who can think systemically, collaborate authentically, and direct technology purposefully. Our graduates don't just succeed—they shape the world they inherit through the power of great thinking amplified by great tools."
	]}
/>

<!-- Our Culture Section -->
<Culture {values} />

<!-- StakeholderGrid Section -->
<StakeholderGrid
	stakeholderType="team"
	title="Meet our founders."
	subtitle="Visionaries shaping the future of education."
	stakeholders={[
		{
			name: "Alexander Zirkler",
			position: "Co-Founder",
			bio: "Educational innovator dedicated to creating learning environments where human creativity and AI capability unite to unlock student potential.",
			image: "https://www.unc.mn/image-placeholder.svg"
		},
		{
			name: "Friederike Seiler",
			position: "Co-Founder",
			bio: "Passionate advocate for authentic assessment and experiential learning, pioneering process-focused education that prepares students for an AI-driven world.",
			image: "https://www.unc.mn/image-placeholder.svg"
		}
	]}
/>

<!-- Partnership Section -->
<StakeholderGrid
	stakeholderType="investor"
	title="Real-world partnerships."
	subtitle="Collaborating with Vienna's leading institutions"
	stakeholders={[
		{
			name: "University of Vienna",
			image: "https://www.unc.mn/image-placeholder.svg"
		},
		{
			name: "Vienna International Centre",
			image: "https://www.unc.mn/image-placeholder.svg"
		},
		{
			name: "Austrian Research Centres",
			image: "https://www.unc.mn/image-placeholder.svg"
		}
	]}
/>

<!-- CTA Section -->
<CallToAction
	title="Schedule your family visit"
	subtitle="Experience the AURA difference firsthand"
	description="Discover how your child can join Vienna's most innovative cohort of students mastering the future of human-AI collaboration. Our Mission Nights showcase real student projects defending their process—see what authentic AI literacy looks like."
	imageSrc="/generated/image-a-warm-candid-scene-of-an-international-.webp"
	callsToAction={[
		{
			href: "/contact",
			label: "Book campus tour",
			variant: "primary"
		},
		{
			href: "/mission-nights",
			label: "Attend Mission Night",
			variant: "secondary"
		}
	]}
/>
