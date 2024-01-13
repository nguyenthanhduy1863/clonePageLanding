<template>
  <div class="relative inline-block">
    <img class=" shadow-2xl w-full xl:h-[300px] xl:h-[450px] rounded-[25px]" :src="props.img"></img>
    <UButton class="px-10 py-3 absolute bottom-7 left-1/2 transform translate-x-[-50%] text-xl rounded-[25px] "> {{ props.name }} </UButton>
  </div>
</template>

<script setup>
  const props = defineProps(['img','name'])
</script>