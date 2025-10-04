<script lang="ts">
	// Components
	import Summary from "$lib/components/layout/Summary.svelte";
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import AboutTeaser from "$lib/components/layout/AboutTeaser.svelte";
	import LogoScroller from "$lib/components/layout/LogoScroller.svelte";
	import Hero from "$lib/components/layout/hero-sections/Hero.svelte";

	// Icons
	import IconActivity from "~icons/lucide/activity";
	import IconBrain from "~icons/lucide/brain";
	import IconZap from "~icons/lucide/zap";
	import IconLineChart from "~icons/lucide/line-chart";
	import IconUsers from "~icons/lucide/users";
	import IconTrendingUp from "~icons/lucide/trending-up";
</script>

<Hero
	centered={false}
	title="Find your calm in the chaos of school, social life, and everything in between"
	subtitle="Real-time biometric insights meet personalized mindfulness to help you navigate stress with confidence and clarity."
	imageSrc="/generated/image-a-confident-teenage-student-stands-smili.webp"
/>
<LogoScroller 
	label="Trusted by leading organizations supporting teen wellness"
	logoUrls={[
		'https://cdn.brandfetch.io/headspace.com/w/400/h/400/logo',
		'https://cdn.brandfetch.io/calm.com/w/400/h/400/logo',
		'https://cdn.brandfetch.io/betterhelp.com/w/400/h/400/logo',
		'https://cdn.brandfetch.io/nami.org/w/400/h/400/logo'
	]}
/>

<Summary
	title="What we do"
	text="OMiE combines real-time biometric monitoring with personalized mindfulness interventions designed specifically for teenage emotional patterns. We help high school and college students manage overwhelming academic and social stress without the cost and scheduling conflicts of traditional therapy. By understanding your unique stress triggers through biometric data, OMiE delivers the right mindfulness technique at exactly the right moment."
/>

<Testimonials
	testimonials={[
		{
			name: "Mariana Rodriguez",
			position: "High school senior",
			company: "Miami, FL",
			quote:
				"During AP exam season, I used to spend hours trying to calm down before I could even study. OMiE helps me get back to baseline in like 5 minutes now. That's time I actually use for studying instead of spiraling.",
			image: "/generated/image-confident-hispanic-teenage-girl-smiling-.webp"
		},
		{
			name: "Kevin Chen",
			position: "College freshman",
			company: "Boston, MA",
			quote:
				"I was about to drop $150 a week on therapy sessions. OMiE caught my stress patterns before they turned into full panic attacks. It's basically saved me from having to miss classes and fall behind.",
			image: "/generated/image-asian-teenage-boy-with-a-confident-relax.webp"
		},
		{
			name: "Aaliyah Washington",
			position: "High school junior",
			company: "Atlanta, GA",
			quote:
				"My parents were looking at therapy options that cost like $200 per session. With OMiE, I get support whenever I need it for way less. Plus I don't have to wait two weeks for an appointment when I'm stressed about a presentation.",
			image: "/generated/image-black-teenage-girl-with-a-warm-authentic.webp"
		}
	]}
/>

<Features
	title="Everything you need to stay grounded"
	subtitle="OMiE combines cutting-edge biometric technology with evidence-based mindfulness practices designed specifically for the pressures teens face every day."
	features={[
		{
			title: "Real-time stress detection",
			description:
				"Your wearable device monitors heart rate variability and stress signals, catching anxiety before it overwhelms you. OMiE sends gentle alerts and personalized interventions the moment your body shows signs of stress.",
			icon: IconActivity,
			imageSrc: "/generated/image-a-teenage-student-smiling-peacefully-wit.webp"
		},
		{
			title: "Teen-specific interventions",
			description:
				"Unlike generic mindfulness apps, OMiE's exercises are designed around teenage emotional patterns and social pressures. Get support that actually understands what you're going through.",
			icon: IconBrain
		},
		{
			title: "On-demand calm",
			description:
				"Access personalized breathing exercises, guided meditations, and grounding techniques instantly without scheduling appointments or paying therapy costs.",
			icon: IconZap,
			imageSrc: "/generated/image-a-confident-teen-studying-calmly-at-a-de.webp"
		},
		{
			title: "Pattern recognition",
			description:
				"Discover what triggers your stress and when you're most vulnerable through intelligent tracking that reveals patterns you didn't know existed.",
			icon: IconLineChart
		},
		{
			title: "Social stress navigator",
			description:
				"Get real-time support for social anxiety with discrete check-ins and quick techniques you can use anywhere, from the classroom to social situations.",
			icon: IconUsers,
			imageSrc: "/generated/image-a-relaxed-teenager-sitting-outdoors-on-a.webp"
		},
		{
			title: "Progress tracking",
			description:
				"Watch your emotional resilience grow with clear metrics that show how you're building mental strength and managing stress more effectively over time.",
			icon: IconTrendingUp
		}
	]}
/>
<AboutTeaser />
<CallToAction
	title="Start your journey to emotional resilience"
	subtitle="Download OMiE today"
	description="Join thousands of teens who've found their calm. Get personalized mindfulness support for less than the cost of a single therapy session. No scheduling conflicts, no waiting lists—just instant access to the tools you need when you need them."
	imageSrc="/generated/image-a-happy-confident-teenage-student-with-a.webp"
	callsToAction={[
		{
			href: "/get-started",
			label: "Get started free",
			variant: "primary"
		},
		{
			href: "/pricing",
			label: "View pricing",
			variant: "secondary"
		}
	]}
/>
