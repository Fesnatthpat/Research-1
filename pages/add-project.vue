<script setup lang="ts">
// ไม่มี logic ในส่วนนี้ แต่สามารถเพิ่มได้หากมีการจัดการข้อมูลหรือ event ต่างๆ
</script>

<template>
    <div class="container mx-auto min-h-[789px]">
        <div class="md:w-full">
            <div class="py-5">
                <div class="text-center text-white text-2xl font-semibold">Add Project</div>
            </div>
            <div class="m-5 flex flex-col gap-y-4 grid md:grid-cols-2 md:gap-4">
                <!-- Fields -->
                <FormField label="ชื่อโปรเจกค์" placeholder="ชื่อโปรเจกค์" type="text" />
                <FormTextarea label="การอ้างอิง" placeholder="การอ้างอิง" />
                <FormTextarea label="บทคัดย่อ (ภาษาไทย)" placeholder="บทคัดย่อ (ภาษาไทย)" />
                <FormTextarea label="Abstract (ภาษาอังกฤษ)" placeholder="Abstract (ภาษาอังกฤษ)" />
                <FormField label="File" type="file" />
                <FormTextarea label="ที่เกี่ยวข้อง" placeholder="ข้อมูลที่เกี่ยวข้อง" />
                <FormTextarea label="สิ่งที่แนบมา" placeholder="ข้อมูลสิ่งที่แนบมา" />
                <select class="select select-bordered w-full">
                    <option disabled selected>Normal</option>
                    <option>Normal Apple</option>
                    <option>Normal Orange</option>
                    <option>Normal Tomato</option>
                </select>

                <!-- Buttons -->
                <div class="">
                    <div class="flex justify-between m-5 "> <!-- เพิ่ม mt-10 -->
                        <button class="btn btn-error text-white">ยกเลิก</button>
                        <button class="btn btn-info text-white">เพิ่ม</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
