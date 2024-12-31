<script setup>
defineProps([ 'label', 'placeholder' ]);
</script>

<template>
    <div>
        <!-- Label -->
        <label class="ml-3">{{ label }}</label>

        <!-- Textarea -->
        <textarea :placeholder="placeholder" class="textarea textarea-bordered textarea-xs w-full h-24 md:h-0">
    </textarea>
    </div>
</template>
