<script lang="ts">
	import content from '../content.json';

	const { featureShowcase } = content;
</script>

<section class="py-20 lg:py-28 space-y-20 px-4">
	{#each featureShowcase as item}
		<div class="grid md:grid-cols-2 gap-12 items-center">
				<div
					class="w-9/12 mx-auto bg-center bg-no-repeat aspect-square bg-cover rounded-xl bg-gray-200 dark:bg-gray-800"
					data-alt={item.alt}
					style="background-image: url('{item.image}')"
				></div>
				<div class="flex flex-col gap-4">
					<h3
						class="text-2xl font-bold text-gray-900 dark:text-white"
					>
						{item.title}
					</h3>
					<p class="text-gray-600 dark:text-gray-400 leading-relaxed">
						{item.description}
					</p>
					<a
						class="text-primary font-semibold hover:underline"
						href={item.link.href}
						>{item.link.label} →</a
					>
				</div>
		</div>
	{/each}
</section>

