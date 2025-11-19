<script lang="ts">
	import content from '../content.json';

	const { metrics } = content;
</script>

<section class="py-20 lg:py-28 px-4 text-center">
	<h2
		class="text-3xl md:text-4xl font-bold text-gray-900 dark:text-white mb-10"
	>
		{metrics.heading}
	</h2>
	<div class="max-w-4xl mx-auto grid grid-cols-1 sm:grid-cols-3 gap-8">
		{#each metrics.items as item}
			<div class="flex flex-col items-center">
				<p class="text-5xl font-black text-primary">{item.value}</p>
				<p class="text-gray-600 dark:text-gray-400 mt-2">
					{item.label}
				</p>
			</div>
		{/each}
	</div>
</section>

