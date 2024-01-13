<template>
    <div class="text-center pt-[40px] px-[30px] xl:px-[200px] grid lg:grid-cols-6 grid-cols-1">
        <div class=" lg:col-span-2">
            <p class=" text-2xl font-extra">Happy Paws</p>
            <p class="py-[20px]">Duis pharetra venenatis felis, ut tincidunt ipsum consequat nec. Fusce et porttitor libero, eu aliquam nisi. Nam finibus ullamcorper semper.</p>
            <div class="flex justify-center">
                <UIcon class="text-[28px] mr-3" name="i-logos:facebook" dynamic />
                <UIcon class="text-[28px] mr-3" name="i-logos:twitter" dynamic />
                <UIcon class="text-[28px] mr-3" name="i-logos:discord-icon" dynamic />
                <UIcon class="text-[28px] mr-3" name="i-logos:youtube-icon" dynamic />
            </div>
            <div class="pt-5">
                <p>+84 123456789</p>
                <p>hello@gmail.com</p>
            </div>
        </div>
        <div class="lg:col-span-1 text-center">
            <p class="text-green-500 text-xl font-medium mb-[20px]">General</p>
            <p class="my-[10px] text-[20px]" v-for="(item, index) in items" :key="i">{{ item.name }}</p>
        </div>
        <div class="lg:col-span-1 md:text-start text-center">
            <p class="text-green-500 text-xl font-medium mb-[20px]">Links</p>
            <p class="my-[10px] text-[20px]" v-for="(item, index) in links" :key="i">{{ item.name }}</p>
        </div>
        <div class="flex flex-col items-center lg:col-span-2">
            <p class="text-center text-green-500 text-xl font-medium mb-[20px]">Gallary</p>
            <div class="grid grid-cols-3">
                    <img class="m-3 rounded-[10px] xl:w-[120px] xl:h-[100px] lg:w-[80px] md:h-[70px] w-[80px] h-[70px]" src="~/assets/dog1.jpg"></img>
                    <img class="m-3 rounded-[10px] xl:w-[120px] xl:h-[100px] lg:w-[80px] md:h-[70px] w-[80px] h-[70px] " src="~/assets/dog1.jpg"></img>
                    <img class="m-3 rounded-[10px] xl:w-[120px] xl:h-[100px] lg:w-[80px] md:h-[70px] w-[80px] h-[70px] " src="~/assets/dog1.jpg"></img>
                    <img class="m-3 rounded-[10px] xl:w-[120px] xl:h-[100px] lg:w-[80px] md:h-[70px] w-[80px] h-[70px] " src="~/assets/dog1.jpg"></img>
                    <img class="m-3 rounded-[10px] xl:w-[120px] xl:h-[100px] lg:w-[80px] md:h-[70px] w-[80px] h-[70px] " src="~/assets/dog1.jpg"></img>
                    <img class="m-3 rounded-[10px] xl:w-[120px] xl:h-[100px] lg:w-[80px] md:h-[70px] w-[80px] h-[70px] " src="~/assets/dog1.jpg"></img>
            </div>
        </div>
    </div>
</template>

<script setup>
    const items = ref(undefined)
    const getData = async()=>{
        try{
            const {data} = await useFetch('/api/general')
            items.value=data.value
        }catch(e){

        }
    }
    getData()

    const links = ref(undefined)
    const getDataLinks = async()=>{
        try{
            const {data} = await useFetch('/api/links')
            links.value=data.value
        }catch(e){

        }
    }
    getDataLinks()
</script>