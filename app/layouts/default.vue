<template>
  <div>
    
    
    <header class="py-6 74px text-center text-gray-900 dark:text-gray-200 border-b dark:border-gray-400 bg-gray-500/30 ">
      <div class="flex items-center justify-around">
        <NuxtLink class="hover:opacity-70 transition" :to="('/')">Home</NuxtLink>
        <NuxtLink class="hover:opacity-70 transition" :to="('/matron-library')">Matron Library</NuxtLink>
        <NuxtLink class="hover:opacity-70 transition" :to="('/contacts')">Contacts</NuxtLink>
        <NuxtLink class="hover:opacity-70 transition" :to="('/ak-list')">Akhanda kiirtan</NuxtLink>
        <NuxtLink class="hover:opacity-70 transition" :to="('/about')">About</NuxtLink>
      </div>
    </header>
    
    
    <main class="min-h-[calc(100vh-74px-124px)]">
      <div class="dark:text-white bg-white dark:bg-gray-800       mx-auto max-w-md xl:max-w-3xl overflow-hidden">
        <slot /> <!-- content -->
      </div>
    </main>
    
    
    <footer class="py-6 74px text-center bg-gray-500/30 border-t dark:border-gray-400">
      <div class="p-4 flex items-center justify-center">
        <ThemeToggle />
      </div>
    </footer>


  </div>
</template>