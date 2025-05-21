<script lang="ts">
	// Types
	import type { PageProps } from "./$types";

	// Components
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import Pricing from "$lib/components/layout/Pricing.svelte";

	// Props
	const { data }: PageProps = $props();
</script>

<Pricing />

<Testimonials
  testimonials={[
    {
      name: "Elsemarie Holt",
      position: "operations director",
      company: "Richter Analytics",
      quote:
        "I was skeptical about the cost at first, but we identified ROI within the first month. Tasks that used to take 6 hours now take 45 minutes.",
      image:
        "/generated/image-a-professional-headshot-of-elsemarie-hol.webp"
    },
    {
      name: "Jabril Mehta",
      position: "head of growth",
      company: "Vecton Systems",
      quote:
        "The platform practically paid for itself in the first quarter. We've replaced 3 tools and eliminated redundant workflows.",
      image:
        "/generated/image-a-professional-headshot-of-jabril-mehta-.webp"
    },
    {
      name: "Nerea Delgado",
      position: "product manager",
      company: "Huronq Technologies",
      quote:
        "I’ve tried dozens of SaaS tools. This was by far the easiest to get started with—and the customer support is exceptional.",
      image:
        "/generated/image-a-professional-headshot-of-nerea-delgado.webp"
    }
  ]}
/>

<CallToAction
  title="Save hours. Close more deals."
  subtitle="Less admin, more selling."
  description="Start automating your outbound workflow to free up time for real conversations and bigger wins. Try it today and see how much more your team can achieve."
  imageSrc="/generated/image-a-delighted-customer-is-using-a-product-.webp"
  callsToAction={[
    {
      href: '/get-started',
      label: 'Start free',
      variant: 'primary'
    },
    {
      href: '/contact',
      label: 'Talk to sales',
      variant: 'secondary'
    }
  ]}
/>
