


<template>

  <div class="m-6 text-xl text-center       border border-dashed border-red-500">
    <h1 class="p-4 text-3xl font-bold">
      {{ error.statusCode || 404 }}
    </h1>
    <div class="p-2">
      {{ error.statusMessage || 'Page not found' }}
    </div>
    <div class="p-2">
      <NuxtLink to="/" >
        <span class="text-xl text-blue-400 hover:text-blue-500 transition ">to main page</span>
      </NuxtLink>
    </div>
  </div>


</template>







<script setup>
const props = defineProps(['error'])
</script>