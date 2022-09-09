<template>
  <nav>
    <h4 class="text-xl">
      <Bars3Icon class="inline-block h-5 w-5 text-blue-500" />
      menu (dans <code class="font-mono">/src/App.vue</code>)
    </h4>
    <ul>
      <li class="flex flex-col">
        <router-link class="text-red-600 underline" to="/">
          lien vers
          <code class="font-mono">/src/pages/index.vue</code>
        </router-link>
        <router-link class="text-red-600 underline" to="/simple">
          lien vers
          <code class="font-mono">/src/pages/simple.vue</code>
        </router-link>
        <router-link class="text-red-600 underline" to="/liste">
          lien vers
          <code class="font-mono">/src/pages/liste.vue</code>
        </router-link>
        <router-link class="text-red-600 underline" to="/liste-fetch">
          lien vers
          <code class="font-mono">/src/pages/liste-fetch.vue</code>
        </router-link>
        <router-link class="text-red-600 underline" to="/654165">
          lien vers
          <code class="font-mono">/src/pages/654165.vue</code>
        </router-link>
      </li>
    </ul>
  </nav>

  <!-- Affiche les pages -->
  <Suspense>
        <template #default>
          <router-view class="m-2 border-2 p-2" />
        </template>
        <template #fallback>
            Chargement...
        </template>
    </Suspense>
</template>

<script setup lang="ts">
import { Bars3Icon } from '@heroicons/vue/20/solid'
</script>
