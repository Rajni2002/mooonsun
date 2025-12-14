<script lang="ts">
	import content from '../content.json';

	const { founderStory } = content;
</script>

<section class="py-20 lg:py-28 px-4">
	<div
		class="max-w-3xl mx-auto flex flex-col md:flex-row items-center gap-8 bg-white dark:bg-gray-800/20 p-8 md:p-12 rounded-xl border border-gray-200 dark:border-gray-800"
	>
		<img
			class="size-24 rounded-full"
			alt={founderStory.alt}
			src={founderStory.image}
			loading="lazy"
			width="96"
			height="96"
		/>
		<div>
			<p
				class="text-2xl font-medium text-gray-900 dark:text-white mb-4"
			>
				{founderStory.greeting}
			</p>
			<p class="text-gray-600 dark:text-gray-400 leading-relaxed">
				{founderStory.description}
			</p>
		</div>
	</div>
</section>

