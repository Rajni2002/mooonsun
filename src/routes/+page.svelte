<script lang="ts">
	import Header from '$lib/components/Header.svelte';
	import Hero from '$lib/components/Hero.svelte';
	import SocialProof from '$lib/components/SocialProof.svelte';
	import Features from '$lib/components/Features.svelte';
	import FeatureShowcase from '$lib/components/FeatureShowcase.svelte';
	// import FounderStory from '$lib/components/FounderStory.svelte';
	import Metrics from '$lib/components/Metrics.svelte';
	import CTA from '$lib/components/CTA.svelte';
	import Footer from '$lib/components/Footer.svelte';
</script>

<Header />
<main class="flex-1">
	<Hero />
	<SocialProof />
	<Features />
	<FeatureShowcase />
	<!-- <FounderStory /> -->
	<Metrics />
	<CTA />
</main>
<Footer />
