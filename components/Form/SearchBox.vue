<script setup lang="ts">
import { Search } from 'lucide-vue-next'
</script>

<template>
    <div class="flex items-center bg-white rounded-lg shadow-md w-full px-3 py-2">
        <Search class="text-gray-500 mr-2" />
        <input type="search" placeholder="Search" class="bg-transparent w-full outline-none text-sm" />
    </div>
</template>

<style scoped></style>
