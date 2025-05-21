<script lang="ts">
	// Types

	// Components
	import SectionHeader from "$lib/components/layout/SectionHeader.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Card from "$lib/components/ui/Card.svelte";
	import JobList, { type JobOpening } from "./JobList.svelte";

	// Icons
	import IconBriefcase from "~icons/lucide/briefcase";
	import IconUsers from "~icons/lucide/users";
	import IconHeart from "~icons/lucide/heart";
	import IconGlobe from "~icons/lucide/globe";

	// Constants
	const SECTION_BASE_CLASSES = "section-py section-px container mx-auto";
	const GRADIENT_BG_CLASSES =
		"bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-900 dark:to-gray-800";
	const ICON_CONTAINER_CLASSES =
		"bg-primary-50 text-primary-600 dark:bg-primary-950 dark:text-primary-400 flex items-center justify-center rounded-full";

	const benefits = [
  {
    title: "Make a real impact",
    description: "Work on real problems and see the results of your effort every day.",
    icon: IconBriefcase
  },
  {
    title: "Grow without limits",
    description: "Learning stipends, mentorship, stretch projects, and the freedom to chart your own path.",
    icon: IconUsers
  },
  {
    title: "Flexibility you can count on",
    description: "Remote-first, flexible hours, and a true respect for work-life balance.",
    icon: IconHeart
  }
];

	const openings: JobOpening[] = [
		// Engineering
		{
			title: "Senior Frontend Developer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Backend Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Design Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Design
		{
			title: "UX/UI Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Product
		{
			title: "Product Manager",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Analyst",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Marketing
		{
			title: "Marketing Specialist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Content Strategist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Social Media Manager",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		}
	];

	const employeeTestimonials = [
  {
    name: "Sofia Martinez",
    position: "Associate Product Manager",
    company: "Product Team",
    quote:
      "It feels like everyone genuinely wants you to succeed—across teams, levels, all of it. That kind of support makes it easy to bring your best every day.",
    image: "/generated/image-a-latina-woman-in-a-contemporary-office-.webp"
  },
  {
    name: "James Okoro",
    position: "Director of Engineering",
    company: "Engineering Team",
    quote:
      "I've grown more in the last 18 months than I did in the five years prior. The leadership track here is clearly mapped, but there's also room to make it your own.",
    image: "/generated/image-a-black-man-in-an-engineering-leadership.webp"
  },
  {
    name: "Emily Nguyen",
    position: "Designer",
    company: "Creative Team",
    quote:
      "I can actually focus here. The tools are solid, meetings have a purpose, and folks respect heads-down time. That vibe? It adds up.",
    image: "/generated/image-a-vietnamese-american-woman-designer-dee.webp"
  }
];

	const processSteps = [
  {
    step: 1,
    title: "Submit your application",
    description: "Send your resume and a few lines about why you’re interested—no cover letter needed."
  },
  {
    step: 2,
    title: "Intro call",
    description: "A short conversation about mutual fit and your career goals."
  },
  {
    step: 3,
    title: "Team interviews",
    description: "Chat with future teammates, discuss your experience, and walk through some practical challenges."
  },
  {
    step: 4,
    title: "Final chat & offer",
    description: "Ask anything—if it’s a fit for both sides, we’ll move fast with a formal offer."
  }
];

	const values = [
  {
    title: "Low-ego, high-trust",
    description: "We hire for curiosity, not ego. Collaboration thrives on candor and support."
  },
  {
    title: "Default open",
    description: "We share information freely and believe everyone’s voice should shape our direction."
  },
  {
    title: "Think systems, not silos",
    description: "Great products come from crossing boundaries—close collaboration beats hierarchy."
  },
  {
    title: "Feedback first",
    description: "Kind, clear feedback is how we get better—no guesswork, just growth."
  },
  {
    title: "Speed with intention",
    description: "We operate quickly, but consciously—respecting thoughtfulness and debate along the way."
  }
];
</script>

<!-- Hero Section -->

<SecondaryHero
	title="Build software that transforms how teams work"
	subtitle="Join caring people, tackle meaningful problems, and shape the future of collaboration"
	imageSrc="/generated/image-a-modern-office-environment-showcasing-a.webp"
/>

<!-- Why Join Us Section -->
<section class={SECTION_BASE_CLASSES}>
	<SectionHeader title="Why join us?" subtitle="Build your career while making an impact" />

	<div class="mt-16 grid gap-4 md:grid-cols-3">
		{#each benefits as benefit}
			<Card {...benefit} />
		{/each}
	</div>
</section>

<!-- Culture Section -->
<Culture {values} />

<Testimonials testimonials={employeeTestimonials} />

<!-- Application Process -->
<section class={SECTION_BASE_CLASSES}>
	<div class="mx-auto">
		<h2 class="text-title1 mb-16">Our application process</h2>

		<div class="grid gap-12 md:grid-cols-3">
			{#each processSteps as { step, title, description }, i}
				<div class="flex flex-col">
					<div class="{ICON_CONTAINER_CLASSES} mb-6 size-11">
						<span class="text-headline">{step}</span>
					</div>
					<h3 class="text-headline mb-3">{title}</h3>
					<p class="text-body text-emphasis-low">{description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>
<!-- Current Openings Section -->
<section class={GRADIENT_BG_CLASSES}>
	<div class="section-px section-py container mx-auto grid w-full items-start lg:grid-cols-2">
		<SectionHeader title="Current openings" subtitle="Find your perfect role" />

		<JobList {openings} />
	</div>
</section>
