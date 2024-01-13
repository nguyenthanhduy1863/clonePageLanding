<template>
        <div class="shadow-2xl inline-flex bg-white rounded-2xl flex-col justify-center items-center sm:p-10 p-10">
            <img class="hover:shadow-xl xl:w-[300px] xl:h-[350px] rounded-[15px]" :src="props.img" />
            <div>
                <p class="text-xl font-bold py-3">Name</p>
                <p class="text-gray-500">Name</p>
            </div>
            <UButton class="rounded-[25px] block mt-5 text-[15px] px-5 py-3">Adopt Now 
                <UIcon class="ml-[10px] text-[20px]" name="i-twemoji:red-heart" dynamic></UIcon>
            </UButton>
        </div>
</template>
<script setup>
    const props = defineProps(['img'])
</script>