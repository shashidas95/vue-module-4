<script setup>
const bgOrange = 'background-color:rgba(251,146, 60,1)'
const bgIndigo = 'background-color:rgba(129,140, 248,1)'
const bgGreen = 'background-color:rgba(52,211,153,1)'
const bgRed = 'background-color:rgba(220,38, 38,1)'
const bgDarkGreen = 'background-color:rgba(5,150, 105,1)'

const Colors = {
  borderColor: 'rgba(20,184,166,1)',
  color: 'rgba(19,78,74,1)',
  backgroundColor: 'rgba(204,251,241,1)',
}
const weekday = true

const messageType = 'error'
if ('error' == messageType) {
  Colors.borderColor = 'rgba(220,38, 38,1)'
  Colors.color = 'rgba(129,140, 248,1)'
  Colors.backgroundColor = 'rgba(204,251,241,1)'
}
</script>
<template>
  <section class="container mx-auto">
    <h1 class="text-center text-2xl py-10">Class & Style Binding</h1>

    <section class="flex space-x-12">
      <div class="w-1/3 h-16" :style="bgOrange"></div>
      <div class="w-1/3 h-16" :style="bgIndigo"></div>
      <div class="w-1/3 h-16" :style="bgGreen"></div>
    </section>

    <section class="mt-10">
      <div
        class="bg-red-600 h-16 flex items-center justify-center text-white"
        :style="
          weekday ? [bgRed, 'font-size: 56px'] : [bgGreen, 'font-seze: 12px']
        "
      >
        It's a weekday!
      </div>
    </section>

    <section class="mt-10">
      <div
        class="border-t-4 rounded-b px-4 py-3 shadow-md"
        role="alert"
        :style="Colors"
      >
        <p class="font-bold">Our privacy policy has changed</p>
        <p class="text-sm">Make sure you know how these changes affect you.</p>
      </div>
    </section>
  </section>
</template>
<style scoped></style>
