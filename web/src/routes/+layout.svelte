<script lang="ts">
  import Header from '$lib/components/Header.svelte'
  import '../app.postcss'
  import { dev } from '$app/environment'
  import { inject } from '@vercel/analytics'

  inject({ mode: dev ? 'development' : 'production' })
</script>

<svelte:head>
  <title>Ask Jamie - AI Powered Cisco Documentation and Knowledgebase</title>
</svelte:head>

<div class="flex min-h-screen flex-col">
  <Header />


  <div id="sticky-banner" tabindex="-1" class="flex top-0 left-0 z-40 justify-between w-full p-2 border-b border-gray-200 bg-orange-50/20 text-xs md:text-sm">
    <div class="flex items-center mx-auto">
        <p class="flex items-center font-normal text-gray-500 dark:text-gray-400">
            <span>This site is not affiliated with Cisco and it is <span class="font-semibold">not</span> an official documentation or support resource!</span>
        </p>
    </div>
</div>


  <main class="flex flex-col flex-1 bg-muted/50 relative">
    <slot />
  </main>
</div>
