<script setup>
defineProps([ 'label', 'placeholder', 'type' ]);
</script>

<template>
    <div>
        <!-- Label -->
        <label class="ml-3">{{ label }}</label>

        <!-- Input -->
        <label class="input input-bordered flex items-center gap-2">
            <input v-if="type !== 'file'" :type="type" :placeholder="placeholder" class="grow" />
            <input v-else type="file" class="grow" />
        </label>
    </div>
</template>
