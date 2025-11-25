<script lang="ts">
	// Components
	import Hero from "$lib/components/layout/hero-sections/Hero.svelte";
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import PricingTable from "$lib/components/layout/PricingTable.svelte";
</script>

<Hero
	title="Meet Tovi, your AI mental health companion"
	subtitle="Chat naturally through iMessage. Get real support for stress, anxiety, and everything in between. No apps, no stigma, just you and Tovi."
	imageSrc="/generated/image-a-genuine-teenage-girl-around-16-sits-on.webp"
	centered={true}
	showPhoneSignup={true}
/>

<Features
	title="How Tovi helps you thrive"
	subtitle="Mental health support that fits into your life"
	features={[
		{
			title: "Chat naturally in iMessage",
			description:
				"No new apps to download. Just text Tovi like you're talking to a friend who really gets you."
		},
		{
			title: "Detect mood patterns",
			description:
				"Tovi notices subtle shifts in your emotions over time, helping you understand what triggers stress or anxiety."
		},
		{
			title: "Get personalized strategies",
			description:
				"Receive coping techniques tailored to your unique situation, not generic advice that never helps."
		},
		{
			title: "Track emotional shifts",
			description:
				"See how your feelings change day to day, and learn what helps you feel better."
		},
		{
			title: "Connect with Apple Health",
			description:
				"Understand how sleep, activity, and daily rhythms affect your mental wellbeing."
		},
		{
			title: "Voice or text journaling",
			description:
				"Express yourself however feels right in the moment, whether that's typing or talking."
		}
	]}
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

<PricingTable
	title="Simple, transparent pricing"
	subtitle="Start free, upgrade when you're ready"
	tiers={[
		{
			name: "Free",
			monthlyPrice: 0,
			yearlyPrice: 0,
			description: "Get started with essential mental health support",
			features: [
				"Unlimited messaging with Tovi",
				"Basic mood tracking",
				"Daily check-ins",
				"Personalized coping strategies",
				"Text and voice journaling"
			],
			cta: {
				label: "Start free",
				href: "/"
			},
			highlight: false
		},
		{
			name: "Premium",
			monthlyPrice: 9.99,
			yearlyPrice: 7.99,
			description: "Advanced insights and personalized coaching",
			features: [
				"Everything in Free",
				"Advanced mood pattern analysis",
				"Apple Health integration",
				"Weekly progress reports",
				"Priority support",
				"Personalized coaching sessions"
			],
			cta: {
				label: "Upgrade to Premium",
				href: "/"
			},
			highlight: true
		},
		{
			name: "School/Organization",
			monthlyPrice: null,
			yearlyPrice: null,
			description: "Mental health support for your entire community",
			features: [
				"Everything in Premium",
				"Bulk licensing for schools or organizations",
				"Admin dashboard and analytics",
				"Custom integration options",
				"Dedicated account manager",
				"Training and onboarding support"
			],
			cta: {
				label: "Contact us",
				href: "/contact"
			},
			highlight: false
		}
	]}
	tierNames={["Free", "Premium", "School/Organization"]}
	features={[
		{
			name: "Messaging with Tovi",
			tiers: {
				Free: "Unlimited",
				Premium: "Unlimited",
				"School/Organization": "Unlimited"
			}
		},
		{
			name: "Mood tracking",
			tiers: {
				Free: "Basic",
				Premium: "Advanced",
				"School/Organization": "Advanced"
			}
		},
		{
			name: "Apple Health integration",
			tiers: {
				Free: false,
				Premium: true,
				"School/Organization": true
			}
		},
		{
			name: "Progress reports",
			tiers: {
				Free: false,
				Premium: "Weekly",
				"School/Organization": "Weekly"
			}
		},
		{
			name: "Personalized coaching",
			tiers: {
				Free: false,
				Premium: true,
				"School/Organization": true
			}
		},
		{
			name: "Admin dashboard",
			tiers: {
				Free: false,
				Premium: false,
				"School/Organization": true
			}
		},
		{
			name: "Support response time",
			tiers: {
				Free: "24 hours",
				Premium: "4 hours",
				"School/Organization": "1 hour"
			}
		}
	]}
/>
