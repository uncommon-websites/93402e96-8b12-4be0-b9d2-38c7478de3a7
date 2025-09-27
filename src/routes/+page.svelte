<script lang="ts">
	// Components
	import Summary from "$lib/components/layout/Summary.svelte";
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import AboutTeaser from "$lib/components/layout/AboutTeaser.svelte";
	import LogoScroller from "$lib/components/layout/LogoScroller.svelte";
	import Hero from "$lib/components/layout/hero-sections/Hero.svelte";
</script>

<Hero
	title="Real school. Real problems. Real outcomes."
	subtitle="Where students think deeply, build boldly, and defend their work."
	imageSrc="/generated/image-a-small-group-of-diverse-international-s.webp"
	centered={false}
/>
<LogoScroller 
	label="Trusted by internationally-minded families from"
	logoUrls={[
		'https://cdn.brandfetch.io/microsoft.com/w/400/h/400/logo',
		'https://cdn.brandfetch.io/un.org/w/400/h/400/logo',
		'https://cdn.brandfetch.io/siemens.com/w/400/h/400/logo',
		'https://cdn.brandfetch.io/bmw.com/w/400/h/400/logo'
	]}
/>

<Summary
	title="A new kind of international school"
	text="Built for globally minded families in Vienna, we prepare students with teacher-led instruction, daily tech-free collaboration blocks, and real-world projects. Students learn to think with AI—never be replaced by it—while developing the critical thinking skills needed for university and life."
/>

<Testimonials
	testimonials={[
		{
			name: "Dr. Elena Marchetti",
			position: "Cultural Attaché",
			company: "Italian Embassy Vienna",
			quote:
				"After three international school transfers, we finally found a place where Maya thrives academically without losing her creativity. The process-based assessment means she's not cramming for tests—she's building real solutions and presenting to actual organizations. Worth every euro for the confidence she's gained.",
			image: "/generated/image-1-headshot-of-a-professional-diplomatic-.webp"
		},
		{
			name: "Prof. Marcus Chen",
			position: "Senior Research Fellow",
			company: "IIASA International Institute",
			quote:
				"As a researcher, I was skeptical about AI in education until I saw how their teachers guide students to direct AI tools rather than depend on them. David went from struggling with traditional homework to presenting a water quality project to Vienna's environmental council. The oral defense model eliminates any cheating concerns.",
			image: "/generated/image-2-headshot-of-a-thoughtful-male-research.webp"
		},
		{
			name: "Fatima Al-Rashid",
			position: "Regional Director",
			company: "Siemens Energy",
			quote:
				"We relocated from Dubai expecting to compromise on education quality, but this school exceeded our expectations. Layla collaborated with actual UNESCO researchers on a refugee integration project—no textbook could teach that. The teacher-led approach with screen-strategic days gives her the best of both worlds.",
			image: "/generated/image-3-headshot-of-a-multinational-businesswo.webp"
		}
	]}
/>

<Features
	title="Why families choose AURA"
	subtitle="The only Vienna school where teachers lead, students direct AI, and real problems meet rigorous academics"
	features={[
		{
			title: "Teacher-led AI integration",
			description: "Expert educators guide students in directing artificial intelligence as a powerful thinking tool, never replacing human creativity and critical reasoning.",
			imageSrc: "/generated/image-a-documentary-style-image-of-a-diverse-s.webp"
		},
		{
			title: "Real-world problem solving",
			description: "Students tackle authentic challenges from Vienna's international community, shipping solutions that matter instead of completing worksheets.",
			imageSrc: "/generated/image-a-candid-image-of-students-presenting-th.webp"
		},
		{
			title: "Process over product assessment",
			description: "Rigorous oral defenses and iterative validation measure deep thinking and problem-solving mastery, preparing students for university and beyond.",
			imageSrc: "/generated/image-a-documentary-style-image-of-students-co.webp"
		},
		{
			title: "Screen-strategic daily rhythm",
			description: "Balanced screen time with daily collaboration blocks ensures digital literacy while preserving essential human connection and social development.",
			imageSrc: "/generated/image-a-warm-documentary-style-scene-of-intern.webp"
		},
		{
			title: "Systems thinking development",
			description: "Students learn to see connections, understand complexity, and approach challenges holistically through our proven Five Pillars methodology.",
			imageSrc: "/generated/image-a-warm-candid-portrait-of-diverse-childr.webp"
		},
		{
			title: "Hands-on creation culture",
			description: "Building prototypes, defending ideas, and iterating solutions develops confident creators who thrive in an uncertain, rapidly changing world.",
			imageSrc: "/generated/image-a-candid-medium-wide-image-of-young-lear.webp"
		}
	]}
/>
<AboutTeaser generating />
<CallToAction generating />
