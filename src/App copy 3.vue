<script setup>
// const items = [1, 2, 3, 4, 5]
const tasks = [
  'API Development and Integration',
  'Database Design and Management',
  'Server-Side Logic Implementation',
  'Performance Optimization',
  'Security and Data Protection',
]
</script>
<template>
  <section
    class="mx-auto container flex items-center text-center flex-col space-y-2"
  >
    <!-- <div class="p-5 border border-gray-600 w-40" v-for="item in items">
      {{ item }}
    </div> -->
    <div
      class="p-5 border text-start border-gray-600 w-full"
      v-for="(task, index) in tasks"
    >
      {{ index + 1 }}.{{ task }}
    </div>
  </section>
</template>
<style scoped></style>
