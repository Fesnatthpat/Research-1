<script setup lang="ts">
import { Search } from 'lucide-vue-next'
</script>

<template>
    <div class="container mx-auto p-4">
        <!-- Search Input -->
        <div class="flex justify-center mb-5 border-b border-t py-2 border-gray-700">
            <div class="flex items-center bg-white rounded-lg shadow-md w-1/2 px-3 py-2">
                <Search class="text-gray-500 mr-2" />
                <input type="search" placeholder="Search" class=" bg-transparent w-full outline-none text-sm" />
            </div>
        </div>
        <!-- Boxes -->
        <div class="flex flex-col gap-y-2 grid md:grid-cols-2 md:gap-2">
            <div class="bg-gray-300 rounded-md w-full h-[100px] text-center text-black font-semibold">
                Box
            </div>
            <div class="bg-gray-300 rounded-md w-full h-[100px] text-center text-black font-semibold">
                Box
            </div>
            <div class="bg-gray-300 rounded-md w-full h-[100px] text-center text-black font-semibold">
                Box
            </div>
            <div class="bg-gray-300 rounded-md w-full h-[100px] text-center text-black font-semibold">
                Box
            </div>
            <!-- <div class="bg-gray-300 rounded-md w-full h-[100px] text-center text-black font-semibold">
                Box
            </div> -->
        </div>
    </div>
</template>

<style scoped></style>
