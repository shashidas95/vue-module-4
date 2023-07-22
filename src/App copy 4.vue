<script setup>
// const items = [1, 2, 3, 4, 5]
const tasks = [
  {
    id: 1,
    title: 'API Development and Integration',
    status: 'finished',
  },
  {
    id: 2,
    title: 'Database Design and Management',
    status: 'active',
  },
  {
    id: 3,
    title: 'Server-Side Logic Implementation',
    status: 'in process',
  },
  {
    id: 4,
    title: 'Performance Optimization',
    status: 'finished',
  },
  {
    id: 5,
    title: 'Security and Data Protection',
    status: 'active',
  },
]
function getCompletedTasks() {
  return tasks.filter((task) => 'finished' == task.status)
}
function getActiveTasks() {
  return tasks.filter((task) => 'active' == task.status)
}
</script>
<template>
  <section
    class="mx-auto container flex items-center text-center flex-col space-y-2"
  >
    <!-- <div class="p-5 border border-gray-600 w-40" v-for="item in items">
      {{ item }}
    </div> -->
    <h2>completed tasks</h2>
    <div
      class="p-5 border text-start border-gray-600 w-full"
      v-for="task in getCompletedTasks()"
      :key="task.id"
    >
      {{ task.id }}.{{ task.title }}
    </div>
    <h2>Active tasks</h2>
    <div
      class="p-5 border text-start border-gray-600 w-full"
      v-for="task in getActiveTasks()"
      :key="task.id"
    >
      {{ task.id }}.{{ task.title }}
    </div>
  </section>
</template>
<style scoped></style>
