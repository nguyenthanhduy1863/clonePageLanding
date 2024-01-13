<template>

    <div class="relative">
        <!-- Header -->
        <div class="fixed z-10 w-full bg-white border-b-[1px] shadow-sm">
            <Header/>
        </div>

        <!-- Main -->
        <div class="pt-[121px]">
            <slot></slot>
        </div>

        <!-- Footer -->
        <div class="border-t-[1px] shadow-sm h-[350px]">
            <Footer />
        </div>
    </div>
</template>