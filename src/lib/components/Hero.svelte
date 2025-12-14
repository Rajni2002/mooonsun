<script lang="ts">
  import CTAtallyButton from "$lib/components/ui/CTAtallyButton.svelte";
  import content from "../content.json";

  const { hero } = content;
</script>

<section
  class="grid grid-cols-1 md:grid-cols-1 items-center gap-12 py-20 lg:py-32 px-4"
>
  <div class="text-center">
    <h1
      class="text-gray-900 dark:text-white text-4xl md:text-6xl font-black leading-tight tracking-tighter mb-4"
    >
      {hero.heading}
    </h1>
    <p
      class="max-w-xl text-gray-600 dark:text-gray-400 text-lg md:text-2xl leading-relaxed mb-8 mx-auto"
    >
      {hero.description}
    </p>
    <div class="flex-wrap gap-4 flex justify-center">
      <CTAtallyButton
        class="flex min-w-[84px] max-w-[480px] cursor-pointer items-center justify-center overflow-hidden rounded-lg h-12 px-6 bg-primary text-white text-base font-bold leading-normal tracking-[0.015em] hover:bg-primary/90 transition-colors"
      >
        <span class="truncate">{hero.primaryCta.label}</span>
      </CTAtallyButton>
    </div>
  </div>
  <div class="md:flex justify-center items-center">
    <video
      class="w-full md:w-10/12 mx-auto bg-center bg-no-repeat aspect-video bg-cover rounded-lg bg-gray-200 dark:bg-gray-800"
      src={hero.video.src}
      muted
      autoplay
      playsinline
      aria-label={hero.video.alt}
      preload="metadata"
    >
      <track kind="captions" />
    </video>
  </div>
</section>
