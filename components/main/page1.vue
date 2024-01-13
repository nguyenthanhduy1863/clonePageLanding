<template>
    <div class="relative">
        <div class="h-[750px] px-[30px] xl:px-[200px] rounded-[25px]">
            <img class="shadow-xl w-full h-full rounded-[25px]" src="~/assets/dogbg.webp" alt="Dog Image"/>
        </div>
        <div class="xl:pl-[250px] md:pl-[30px] pl-[50px]  sm:w-3/4 lg:w-1/2 absolute  top-1/2 transform -translate-y-1/2">
            <p class="text-green-500 font-semibold text-[18px]">ADOPT A PET</p>
            <p class="text-blue-500 text-[30px] font-bold">Thousands Of Homeless Dogs, One Act Of Kindness</p>
            <p class="text-gray-400 pb-5 text-[16px] font-medium">Find your new furry friend today! We have a wide variety of lovable pets available for adoption. Come visit us and take home your new best friend!</p>
            <UButton class="p-3 rounded-[20px] text-[20px]">Adopt now
                <UIcon name="i-emojione:dog-face" dynamic/>
            </UButton>
        </div>
    </div>
</template>
