<template>
    <div class="px-[15px] xl:px-[200px] py-[100px] bg-green-100 text-center">
        <div class="">
            <p class=" font-bold text-3xl mb-4">Small Gesture For A Big Impact</p>
            <p class=" mb-4">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam vitae congue tortor.</p>
        </div>
            <div class="sm:p-[25px] p-2 grid xl:grid-cols-4 md:grid-cols-2 grid-cols-1 "  >
                <MainItemp4 class="mb-5 mx-2" v-for="(item, index) in items" :key="index" :img="item.url"/>
            </div>
    </div>
</template>

<script setup>
    const items = ref(undefined)

    const getData = async()=>{
        try{
            const {data} = await useFetch('/api/imgList')
            items.value = data.value
        }catch(e){

        }
    }
    getData()
</script>