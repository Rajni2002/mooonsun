<script lang="ts">
	import content from '../content.json';

	const { features } = content;
</script>

<section id="features" class="py-20 lg:py-28 px-4">
	<div class="text-center max-w-2xl mx-auto mb-12">
		<h2
			class="text-gray-900 dark:text-white text-3xl md:text-4xl font-bold leading-tight tracking-tight"
		>
			{features.heading}
		</h2>
		<p class="mt-4 text-gray-600 dark:text-gray-400">
			{features.description}
		</p>
	</div>
	<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
		{#each features.items as item}
			<div
				class="bg-white dark:bg-gray-800/20 p-6 rounded-xl border border-gray-200 dark:border-gray-800"
			>
				<div
					class="flex items-center justify-center size-12 rounded-lg bg-primary/10 text-primary mb-4"
				>
					<span class="material-symbols-outlined">{item.icon}</span>
				</div>
				<h3
					class="text-lg font-bold text-gray-900 dark:text-white mb-2"
				>
					{item.title}
				</h3>
				<p class="text-gray-600 dark:text-gray-400">
					{item.description}
				</p>
			</div>
		{/each}
	</div>
</section>

