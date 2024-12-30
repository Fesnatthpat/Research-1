<script setup lang="ts">
import { ref, onMounted } from "vue";

// ตั้งค่าตัวแปรสำหรับสไลด์รูปภาพ
const slides = [
    "https://images.unsplash.com/photo-1733235014927-32494ec8233b?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
    "https://plus.unsplash.com/premium_photo-1733514691555-f6753d15df38?q=80&w=2071&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
    "https://plus.unsplash.com/premium_photo-1733514692194-b7fa81796293?q=80&w=2071&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
    "https://plus.unsplash.com/premium_photo-1733514691626-5493d07ec871?q=80&w=2071&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
    "https://plus.unsplash.com/premium_photo-1733514691452-9d2b1115338a?q=80&w=2069&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
    "https://plus.unsplash.com/premium_photo-1733514692198-89d29a884616?q=80&w=2071&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
];
const currentSlide = ref(0);

onMounted(() => {
    const interval = setInterval(() => {
        nextSlide();
    }, 3000); // เลื่อนอัตโนมัติทุก 3 วินาที

    return () => clearInterval(interval); // หยุดการเลื่อนเมื่อออกจากหน้า
});

const nextSlide = () => {
    currentSlide.value = (currentSlide.value + 1) % slides.length;
};

const prevSlide = () => {
    currentSlide.value =
        (currentSlide.value - 1 + slides.length) % slides.length;
};
</script>

<template>
    <div class="container mx-auto">
        <div class="mx-2 mt-5">
            <div class="carousel w-full h-[200px] relative overflow-hidden">
                <!-- สไลด์ -->
                <div v-for="(slide, index) in slides" :key="index"
                    class="carousel-item w-full absolute transition-all duration-500" :class="{
                        'opacity-100 z-10': currentSlide === index,
                        'opacity-0 z-0': currentSlide !== index,
                    }">
                    <img :src="slide" alt="Slide Image" class="w-full h-[200px] object-cover rounded-md" />
                </div>

                <!-- ปุ่มกดเลื่อนไปข้างหน้า/ถอยหลัง -->
                <div class="absolute left-0 right-0 top-1/2 flex -translate-y-1/2 transform justify-between z-20">
                    <button @click="prevSlide"
                        class="btn btn-circle border-none bg-transparent  text-black p-2 rounded-full shadow-md hover:bg-gray-200">
                        ❮
                    </button>
                    <button @click="nextSlide"
                        class="btn btn-circle border-none bg-transparent  text-black p-2 rounded-full shadow-md hover:bg-gray-200">
                        ❯
                    </button>
                </div>
            </div>
        </div>
    </div>
    <CardsItems />
</template>

<style scoped>
/* ใช้ transition เพื่อให้การเปลี่ยนสไลด์ดูนุ่มนวล */
.carousel-item {
    opacity: 0;
    z-index: 0;
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    transition: opacity 0.5s ease-in-out, z-index 0.5s ease-in-out;
}

.carousel-item.opacity-100 {
    opacity: 1;
    z-index: 10;
}

.btn {
    cursor: pointer;
}
</style>
