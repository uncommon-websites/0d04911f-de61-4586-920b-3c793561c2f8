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
	title="Your mental health matters, and you don't have to figure it out alone"
	subtitle="Chat naturally in iMessage with an AI companion that actually gets you, tracks your mood patterns, and helps you build real coping strategies for stress, anxiety, and everything in between."
	imageSrc="/generated/image-a-candid-portrait-of-a-diverse-teen-visi.webp"
	centered={false}
/>
<LogoScroller
	label="Trusted by the wellness community"
	logoUrls={[
		'https://cdn.brandfetch.io/headspace.com/w/400/h/400/logo',
		'https://cdn.brandfetch.io/betterhelp.com/w/400/h/400/logo',
		'https://cdn.brandfetch.io/talkspace.com/w/400/h/400/logo',
		'https://cdn.brandfetch.io/calm.com/w/400/h/400/logo'
	]}
/>

<Summary
	title="Mental health support, right in your texts"
	text="We're an AI companion that lives in iMessage, so you can check in on your feelings as easily as texting a friend. Whether you're dealing with stress from school, anxiety about the future, or just feeling off, we help you understand your patterns and build strategies that actually work for you. No apps to download, no stigma, just real support when you need it."
/>

<Testimonials
	testimonials={[
		{
			name: "Priya Mehta",
			position: "College Student",
			company: "UC Berkeley",
			quote:
				"I used to wait weeks for therapy appointments when I was really struggling. Now I can talk through anxiety the moment it hits, right in iMessage. It's like having support in my pocket 24/7 without the $200/session price tag.",
			image: "/generated/image-medium-close-portrait-of-a-south-asian-t.webp"
		},
		{
			name: "Marcus Thompson",
			position: "High School Senior",
			company: "Oakland High School",
			quote:
				"Before this, I'd bottle everything up until it got really bad. The mood tracking caught my stress spiraling way earlier, and I learned actual coping techniques instead of just scrolling TikTok at 2am. Honestly saved me from some dark places.",
			image: "/generated/image-medium-close-portrait-of-a-black-teenage.webp"
		},
		{
			name: "Sofia Ramirez",
			position: "College Freshman",
			company: "Stanford University",
			quote:
				"The fact that it's free and just lives in iMessage made it so easy to start. No awkward app downloads, no insurance hassles, no judgment. I've learned more about managing my anxiety in three months than I did in years of avoiding the problem.",
			image: "/generated/image-medium-close-portrait-of-a-hispanic-teen.webp"
		}
	]}
/>

<Features
	title="Built for how you actually live"
	subtitle="Real support that meets you where you are, right in your messages"
	features={[
		{
			title: "Chat naturally in iMessage",
			description:
				"No new apps to download or accounts to create. Just text like you're talking to a friend who really listens and understands what you're going through."
		},
		{
			title: "Spot patterns before you do",
			description:
				"Our AI notices subtle shifts in your mood over time, helping you see triggers and patterns you might miss on your own."
		},
		{
			title: "Get strategies that actually work",
			description:
				"Personalized coping techniques that adapt to your unique situation, not generic advice that sounds good but never helps."
		},
		{
			title: "Connect with your whole wellness",
			description:
				"Integrates with Apple Health to understand how sleep, activity, and daily rhythms affect how you feel."
		},
		{
			title: "Express yourself your way",
			description:
				"Voice notes when you can't type, text when you need to think through it. Journal however feels right in the moment."
		},
		{
			title: "Matches how you talk",
			description:
				"Learns your language and tone over time, so conversations feel natural instead of robotic or overly clinical."
		}
	]}
/>
<AboutTeaser />
<CallToAction
	title="Your next conversation could change everything"
	subtitle="Start for free, no app required"
	description="You don't need to wait for a therapy appointment or figure this out alone. Text us right now in iMessage and start building strategies that actually help. Free to start, zero judgment, always in your pocket when you need support most."
	imageSrc="/generated/image-a-genuine-teen-age-15-19-sits-quietly-ou.webp"
	callsToAction={[
		{
			href: "/",
			label: "Start chatting now",
			variant: "primary"
		},
		{
			href: "/about",
			label: "Learn how it works",
			variant: "secondary"
		}
	]}
/>
