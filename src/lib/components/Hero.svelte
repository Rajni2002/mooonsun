<script lang="ts">
  import CTAtallyButton from "$lib/components/ui/CTAtallyButton.svelte"
  import content from "../content.json";

  const { hero } = content;
</script>

<section class="grid md:grid-cols-2 items-center gap-12 py-20 lg:py-32 px-4">
  <div class="text-center md:text-left">
    <h1
      class="text-gray-900 dark:text-white text-4xl md:text-6xl font-black leading-tight tracking-tighter mb-4"
    >
      {hero.heading}
    </h1>
    <p
      class="max-w-xl text-gray-600 dark:text-gray-400 text-lg md:text-xl leading-relaxed mb-8 mx-auto md:mx-0"
    >
      {hero.description}
    </p>
    <div class="flex-wrap gap-4 flex justify-center md:justify-start">
      <CTAtallyButton
        class="flex min-w-[84px] max-w-[480px] cursor-pointer items-center justify-center overflow-hidden rounded-lg h-12 px-6 bg-primary text-white text-base font-bold leading-normal tracking-[0.015em] hover:bg-primary/90 transition-colors"
      >
        <span class="truncate">{hero.primaryCta.label}</span>
      </CTAtallyButton>
      <CTAtallyButton
        class="flex min-w-[84px] max-w-[480px] cursor-pointer items-center justify-center overflow-hidden rounded-lg h-12 px-6 bg-gray-200 dark:bg-gray-800 text-gray-800 dark:text-white text-base font-bold leading-normal tracking-[0.015em] hover:bg-gray-300 dark:hover:bg-gray-700 transition-colors"
      >
        <span class="truncate">{hero.secondaryCta.label}</span>
      </CTAtallyButton>
    </div>
  </div>
  <div class="hidden md:flex justify-center items-center">
    <div
      class="w-full max-w-md aspect-square bg-gray-200 dark:bg-gray-800 rounded-xl flex items-center justify-center"
    >
      <svg
        class="size-24 text-gray-400 dark:text-gray-600"
        fill="none"
        stroke="currentColor"
        stroke-linecap="round"
        stroke-linejoin="round"
        stroke-width="2"
        viewbox="0 0 24 24"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path d="M22 12h-4l-3 9L9 3l-3 9H2"></path>
      </svg>
    </div>
  </div>
</section>
