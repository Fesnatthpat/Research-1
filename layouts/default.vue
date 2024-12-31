<script setup lang="ts">

</script>

<template>
    <div>
        <AppNavbar-Top />
        <div class="md:min-h-[789px]">
            <slot />
        </div>
        <AppBar-Menu />
    </div>
</template>

<style scoped></style>