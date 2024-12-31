<script setup lang="ts">
import { CirclePlus } from 'lucide-vue-next';
import { House } from 'lucide-vue-next';
import { UserPen } from 'lucide-vue-next';
import { Settings } from 'lucide-vue-next';
import { LayoutDashboard } from 'lucide-vue-next'
</script>

<template>
    <nav class=" fixed bottom-2 right-0 left-0 m-5   rounded-full backdrop-blur-lg bg-transparent/10 drop-shadow-lg">
        <ul class="flex justify-between items-center px-4 py-2 text-white">
            <NuxtLink to="/" class="group flex-1 flex flex-col items-center justify-center transition">
                <House class="h-6 w-6 mb-1 group-hover:scale-110 transition"/>
                <!-- <span>Home</span> -->
            </NuxtLink>
            <li class="group flex-1 flex flex-col items-center justify-center transition">
                <LayoutDashboard class="  h-6 w-6  mb-1 group-hover:scale-110 transition"/>
            </li>
            <NuxtLink to="/Adds/addpage" class="group flex-1 flex flex-col items-center justify-center transition">
                <CirclePlus class=" h-10 w-10 mb-1 group-hover:scale-110 transition"/>
            </NuxtLink>
            <li class="group flex-1 flex flex-col items-center justify-center transition">
                <UserPen class="  h-6 w-6 mb-1 group-hover:scale-110 transition"/>
            </li>
            <li class="group flex-1 flex flex-col items-center justify-center transition">
                <Settings class="  h-6 w-6 mb-1 group-hover:scale-110 transition"/>
            </li>
        </ul>
    </nav>
</template>

<style scoped></style>
