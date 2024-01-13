<template>
    <div class="px-[15px] xl:px-[200px] py-[100px] bg-green-100 text-center">
        <div class="">
            <p class=" font-bold text-3xl mb-4">Small Gesture For A Big Impact</p>
            <p class=" mb-4">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam vitae congue tortor.</p>
            <UButton class="py-3 rounded-[25px] mb-5 inline-block">Meet Theme All 
            </UButton>
        </div>
        <div class="">
            <div class="sm:p-[25px] p-2 grid xl:grid-cols-4 md:grid-cols-2 grid-cols-1 "  >
                <MainItemp4 class="mb-5 mx-2" v-for="(item, index) in test" :key="index" :img="item.url"/>
            </div>
        </div>
    </div>
</template>

<script setup>

const test = ref(undefined)

const getData = async () => {
    try {
        const {data} = await useFetch('/api/imgHome')
        test.value = data.value
    }
    catch(e){
        
    }
}

getData()

</script>