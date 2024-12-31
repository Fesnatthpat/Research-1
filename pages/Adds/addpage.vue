<script setup lang="ts">

</script>

<template>
    <div class=" bg-white">
        <div class="py-5 ">
            <div class="text-center text-black text-2xl font-semibold">Add Project</div>
        </div>
        <div class="m-5 flex flex-col gap-y-2">

            <label class=" ml-3" for="">ชื่อโปรเจกค์</label>
            <label class="input input-bordered flex items-center gap-2">
                <input type="text" class="grow" placeholder="ชื่อโปรเจกค์" />
            </label>

            <label class=" ml-3" for="">การอ้างอิง</label>
            <textarea placeholder="การอ้างอิง" class="textarea textarea-bordered textarea-xs w-full h-24">
            </textarea>

            <label class=" ml-3" for="">บทคัดย่อ(ภาษาไทย)</label>
            <textarea placeholder="บทคัดย่อ(ภาษาไทย)" class="textarea textarea-bordered textarea-xs w-full h-24">
            </textarea>

            <label class=" ml-3" for="">Abstract(ภาษาอังกฤษ)</label>
            <textarea placeholder="บทคัดย่อ(ภาษาไทย)" class="textarea textarea-bordered textarea-xs w-full h-24">
            </textarea>

            <label class=" ml-3" for="">file</label>
            <label class="input input-bordered flex items-center gap-2">
                <input type="file" class="grow" value="file" />
            </label>

            <label class=" ml-3" for="">ที่เกี่ยวข้อง</label>
            <textarea placeholder="บทคัดย่อ(ภาษาไทย)" class="textarea textarea-bordered textarea-xs w-full h-24">
            </textarea>

            <label class=" ml-3" for="">สิ่งที่แนบมา</label>
            <textarea placeholder="บทคัดย่อ(ภาษาไทย)" class="textarea textarea-bordered textarea-xs w-full h-24">
            </textarea>

            <div class="flex justify-between  m-5 h-48">
                <button class="btn btn-error text-white">ยกเลิก</button>
                <button class="btn btn-info text-white">เพิ่ม</button>
            </div>
        </div>
    </div>
</template>

<style scoped></style>