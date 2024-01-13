<template>
    <div class="px-[30px] xl:px-[200px]">
        <div class="pt-[80px] pb-[50px] flex flex-col justify-between items-center">
            <p class="text-green-500 uppercase pb-3">Get Involved</p>
            <p class="font-bold text-[25px] pb-4">Small gesture For A Big Impact</p>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing ElementInternals.</p>
        </div>
        <div class="grid md:grid-cols-3 px-[100px] sm:px-[100px] lg:px-[30px]  grid-cols-1">
            <MainItemp2 class="col-span-1 m-2" v-for="(item, index) in test" :key="index" :img="item.img" :name="item.name"/>
        </div>
        <div class="border-b-[1px] pt-[100px] mb-[100px] w-[70%] mx-auto"></div>
    </div>
</template>

<script setup>


const test = ref(undefined)

const getData = async () => {
    try {
        const {data} = await useFetch('/api/test')
        test.value = data.value
    }
    catch(e){
        
    }
}

getData()

</script>