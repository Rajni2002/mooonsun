<script lang="ts">
	import content from '../content.json';
	import logo from '$lib/assets/logo.svg';
  	import CTAtallyButton from './ui/CTAtallyButton.svelte';

	const { header } = content;
</script>

<header
	class="sticky top-0 z-50 flex items-center justify-between whitespace-nowrap border-b border-solid border-gray-200/80 dark:border-white/10 bg-background-light/80 dark:bg-background-dark/80 backdrop-blur-sm px-6 py-3"
>
	<div class="flex items-center gap-4 text-gray-900 dark:text-white">
		<!-- <div class="size-6 text-primary"> -->
			<img
				class="w-52"
				alt="Mooonsun logo"
				src={logo}
				width="208"
				height="48"
			/>
		<!-- </div> -->
		<!-- <h2
			class="text-gray-900 dark:text-white text-lg font-bold leading-tight tracking-[-0.015em]"
		>
			{brand.name}
		</h2> -->
	</div>
	<div class="hidden md:flex flex-1 justify-end gap-8">
		<nav class="flex items-center gap-9" aria-label="Main navigation">
			{#each header.nav as item}
				<a
					class="text-gray-600 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white text-sm font-medium leading-normal"
					href={item.href}
					aria-label={`Navigate to ${item.label}`}
					>{item.label}</a
				>
			{/each}
		</nav>
		<CTAtallyButton
			class="flex min-w-[84px] max-w-[480px] cursor-pointer items-center justify-center overflow-hidden rounded-lg h-10 px-4 bg-primary text-white text-sm font-bold leading-normal tracking-[0.015em] hover:bg-primary/90 transition-colors"
		>
			<span class="truncate">{header.cta.label}</span>
		</CTAtallyButton>
	</div>
</header>

