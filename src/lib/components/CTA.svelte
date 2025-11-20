<script lang="ts">
	import content from '../content.json';
  import CTAtallyButton from './ui/CTAtallyButton.svelte';

	const { cta } = content;
</script>

<section
	class="py-20 lg:py-32 px-4 bg-gray-100 dark:bg-gray-800/20 rounded-t-xl"
>
	<div class="text-center max-w-2xl mx-auto">
		<h2
			class="text-3xl md:text-4xl font-bold text-gray-900 dark:text-white"
		>
			{cta.heading}
		</h2>
		<p class="text-gray-600 dark:text-gray-400 mt-4 mb-8">
			{cta.description}
		</p>
		<CTAtallyButton
			class="flex min-w-[84px] w-full sm:w-auto mx-auto max-w-[480px] cursor-pointer items-center justify-center overflow-hidden rounded-lg h-12 px-6 bg-primary text-white text-base font-bold leading-normal tracking-[0.015em] hover:bg-primary/90 transition-colors"
		>
			<span class="truncate">{cta.button.label}</span>
		</CTAtallyButton>
		<p class="text-xs text-gray-500 dark:text-gray-500 mt-4">
			{cta.disclaimer}
		</p>
	</div>
</section>

