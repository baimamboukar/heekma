<template>
  <div
    class="grid min-h-screen w-full md:grid-cols-[220px_1fr] lg:grid-cols-[280px_1fr]"
  >
    <!-- Sidebar Content Goes here -->
    <Sidebar />
    <!-- Sidebar Content Goes here -->

    <div class="flex flex-col">
      <!-- Header Content Goes here -->
      <Navbar />
      <!-- Header Content Goes here -->

      <!-- Displaying Current Page -->
      <main class="flex flex-1 flex-col gap-4 p-4 lg:gap-6 lg:p-6">
        <slot />
      </main>
      <!-- Displaying current Page -->
    </div>
  </div>
</template>
