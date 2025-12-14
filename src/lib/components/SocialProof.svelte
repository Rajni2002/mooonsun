<script lang="ts">
	import content from '../content.json';

	const { socialProof } = content;
</script>

<section class="py-12 px-4">
	<p
		class="text-gray-500 dark:text-gray-400 text-sm font-normal leading-normal text-center mb-6"
	>
		{socialProof.text}
	</p>
	<div class="flex justify-center items-center gap-8 md:gap-12 flex-wrap">
		{#each socialProof.logos as logo}
			<img
				class="h-8 opacity-50 dark:opacity-40"
				alt={logo.alt}
				src={logo.src}
				loading="lazy"
				width="120"
				height="32"
			/>
		{/each}
	</div>
</section>

