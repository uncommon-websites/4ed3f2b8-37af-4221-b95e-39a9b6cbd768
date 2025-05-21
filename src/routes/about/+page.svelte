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
    title: "Collaboration",
    description:
      "We’re a team of builders, thinkers, and tinkerers who believe great work starts with trust and curiosity. Collaboration isn’t a buzzword—it’s the way things get done. Engineers work alongside designers and product leads from Day 1. Feedback flows freely. Ideas come from anywhere."
  },
  {
    title: "Well-being",
    description:
      "Our culture is built on shared momentum. We move fast, but not at the cost of balance. Everyone's encouraged to take time off, block heads-down hours, and log off when the day is done."
  },
  {
    title: "Innovation & Inclusion",
    description:
      "Innovation isn’t scheduled—we make space for it. That means time to experiment, plenty of Slack shoutouts for new ideas, and leadership that genuinely wants your input. Diversity, equity, and inclusion aren’t side efforts—they shape every part of how we hire, communicate, and build. Day to day, it’s high-context, low-ego. We celebrate real wins, own our mistakes, and default to optimism."
  },
];
</script>

<SecondaryHero
	title="No one left hungry"
	subtitle="Scaling practical, proven solutions community by community"
	imageSrc="/generated/image-a-diverse-team-collaborating-in-a-spacio.webp"
/>

<!-- Story Section -->
<Story
	paragraphs={[
		"Our company began with one clear vision: to help end world hunger. We saw how many families struggled to find their next meal and decided something had to change.",
		"We believe that solving this problem takes practical steps—bringing together science, community support, and real-world know-how. Every project we take on aims to put food on tables and empower people to thrive.",
		"This mission motivates us daily. While the challenge is big, we measure success by each person we help. For us, even one less empty plate makes it all worth it."
	]}
/>

<!-- Our Culture Section -->
<Culture {values} />

<!-- StakeholderGrid Section -->
<!-- Team section intentionally removed: no team members to display. -->

<!-- Investors section intentionally removed: no investors to display. -->

<!-- CTA Section -->
<CallToAction
  title="Join the way we work"
  subtitle="Curious, collaborative, and ready for the next challenge?"
  description="We're building modern collaboration software for product teams—designed to simplify workflows and help teams move faster, together. If you're a designer, engineer, strategist, or builder who’s curious and collaborative, we’d love to hear from you. Explore our open roles or reach out to start a conversation."
  imageSrc="/generated/image-a-welcoming-and-diverse-team-sharing-a-l.webp"
  callsToAction={[
    { href: "/careers", label: "Explore careers", variant: "primary" },
    { href: "/contact", label: "Contact us", variant: "secondary" },
  ]}
/>
