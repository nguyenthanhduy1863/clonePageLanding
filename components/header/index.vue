<template>
    <div class="h-[120px] px-[30px] xl:px-[200px] flex justify-between items-center">
        <!-- Left -->
        <div class="flex justify-between items-center">
            <!-- <img class="my-auto w-[30px] h-[20px]" src="~/assets/dog1.jpg"></img> -->
            <p class="cursor-pointer text-primary-500 font-extrabold text-3xl" @click="navigateTo('/')">Happy Paws</p>
        </div>

        <!-- Right -->
        <div class="flex">
            <UButton class="hidden md:block px-5 py-3 mx-2 rounded-[20px]">
                <NuxtLink to="/">Home</NuxtLink>
            </UButton>
            <UButton class="hidden md:block hover:bg-gray-50 px-5 py-3 text-green-500 bg-white mx-2"> 
                <NuxtLink to="/menu">Adopt Now</NuxtLink>
            </UButton>
            <UButton class="hidden md:block px-5 py-3 text-[15px] mx-2 rounded-[20px]">
                Try Now
                <UIcon class="text-[25px]" name="i-mdi:pine-tree" dynamic />
            </UButton>
            <UButton class="hover:bg-gray-50 bg-white px-5 py-3 mx-2">
                <UIcon class="text-green-500 text-[25px]" name="i-material-symbols-light:sunny" dynamic />
            </UButton>
            <UButton class="rounded-[20px] px-5 py-3 mx-2">
                <UIcon name="i-ic:baseline-menu" dynamic/>
            </UButton>
        </div>
    </div>
</template>

<script setup>
</script>