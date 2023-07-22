<script setup>
const persons = [
  {
    id: 1,
    name: 'Jane Doe',
    profilePhoto:
      '//tailus.io/sources/blocks/classic/preview/images/woman1.jpg',
    jobTitle: 'CEO, Co-Founder',
  },
  {
    id: 2,
    name: 'John Doe',
    profilePhoto: '//tailus.io/sources/blocks/classic/preview/images/man.jpg',
    jobTitle: 'CTO',
  },
  {
    id: 3,
    name: 'Jessy Doe',
    profilePhoto: '//tailus.io/sources/blocks/classic/preview/images/woman.jpg',
    jobTitle: 'COO',
  },
]
</script>
<template>
  <section class="mx-auto container flex items-center text-center flex-col">
    <div class="p-5 border border-gray-600 w-40">1</div>
    <div class="p-5 border-1 border-gray-600">2</div>
    <div class="p-5 border-1 border-gray-600">3</div>
    <div class="p-5 border-1 border-gray-600">4</div>
    <div class="p-5 border-1 border-gray-600">5</div>
  </section>
  <div class="py-20 bg-gray-50">
    <div class="container mx-auto px-6 px-32">
      <div class="mb-16 text-center">
        <h2 class="mb-4 text-center text-2xl text-gray-900 font-bold text-4xl">
          Team Member
        </h2>
        <p class="text-gray-600 w-8/12 mx-auto">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Magni
          deleniti veniam laudantium itaque perferendis dolor maxime incidunt
          voluptatem.
        </p>
      </div>
      <div class="grid gap-12 items-center grid-cols-3">
        <div
          class="space-y-4 text-center"
          v-for="person in persons"
          :key="person.id"
        >
          <img
            class="w-64 h-64 mx-auto object-cover rounded-xl w-64"
            :class="2 == person.id ? 'h-80' : 'h-64'"
            :src="person.profilePhoto"
          />
          <div>
            <h4 class="text-2xl text-sm text-gray-500">{{ person.name }}</h4>
            <span class="block text-sm text-gray-500">{{
              person.jobTitle
            }}</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped></style>
