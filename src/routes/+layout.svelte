<script lang="ts">
  import favicon from "$lib/assets/favicon.ico";
  import favicon16 from "$lib/assets/favicon-16x16.png";
  import favicon32 from "$lib/assets/favicon-32x32.png";
  import iconApple from "$lib/assets/apple-touch-icon.png";
  import webManifest from "$lib/assets/site.webmanifest";
  import { injectAnalytics } from "@vercel/analytics/sveltekit";
  import { injectSpeedInsights } from '@vercel/speed-insights/sveltekit';
  import { dev } from "$app/environment";
  import content from "../lib/content.json";
  import Seo from "$lib/components/Seo.svelte";

  const { metaInfo } = content;

  let { children } = $props();
  // Inject the Analytics functionality
  injectAnalytics({ mode: dev ? "development" : "production" });
  if(!dev){
    injectSpeedInsights()
  }
</script>

<Seo metatag={metaInfo} />

<svelte:head>
  <link rel="icon" href={favicon} />
  <link rel="apple-touch-icon" sizes="180x180" href={iconApple} />
  <link rel="icon" type="image/png" sizes="32x32" href={favicon32} />
  <link rel="icon" type="image/png" sizes="16x16" href={favicon16} />
  <link rel="manifest" href={webManifest} />
  <meta name="apple-mobile-web-app-capable" content="yes" />
  <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent" />
  <meta name="apple-mobile-web-app-title" content="Mooonsun" />
  <meta name="mobile-web-app-capable" content="yes" />
  <script
    src="https://cdn.tailwindcss.com?plugins=forms,container-queries"
  ></script>
  <link href="https://fonts.googleapis.com" rel="preconnect" />
  <link crossorigin="" href="https://fonts.gstatic.com" rel="preconnect" />
  <link href="https://tally.so" rel="dns-prefetch" />
  <link
    href="https://fonts.googleapis.com/css2?family=Be+Vietnam+Pro:wght@400;500;700;900&display=swap"
    rel="stylesheet"
  />
  <link
    href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined"
    rel="stylesheet"
  />
  <script async src="https://tally.so/widgets/embed.js"></script>
  <script>
    tailwind.config = {
      darkMode: "class",
      theme: {
        extend: {
          colors: {
            primary: "#0500f1",
            "background-light": "#fffff3",
            "background-dark": "#0f231c",
          },
          fontFamily: { display: "Be Vietnam Pro" },
          borderRadius: {
            DEFAULT: "0.5rem",
            lg: "1rem",
            xl: "1.5rem",
            full: "9999px",
          },
        },
      },
    };
  </script>
  <style>
    .material-symbols-outlined {
      font-variation-settings:
        "FILL" 0,
        "wght" 400,
        "GRAD" 0,
        "opsz" 24;
    }
  </style>
</svelte:head>

<div
  class="bg-background-light dark:bg-background-dark font-display text-gray-800 dark:text-gray-200"
>
  <div
    class="relative flex h-auto min-h-screen w-full flex-col overflow-x-hidden"
  >
    <div class="layout-container flex h-full grow flex-col">
      <div class="flex flex-1 justify-center">
        <div class="layout-content-container flex flex-col w-full max-w-6xl">
          {@render children()}
        </div>
      </div>
    </div>
  </div>
</div>
<!-- extend: {
					colors: {
						primary: '#019863',
						'background-light': '#f5f8f7',
						'background-dark': '#0f231c',
					},
					fontFamily: { display: 'Be Vietnam Pro' },
					borderRadius: {
						DEFAULT: '0.5rem',
						lg: '1rem',
						xl: '1.5rem',
						full: '9999px',
					},
				}, -->
