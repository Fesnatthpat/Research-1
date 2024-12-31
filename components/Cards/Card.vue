<script setup lang="ts">
import { ref, onMounted } from 'vue'

// กำหนดประเภทของข้อมูลในโปรเจกต์
interface Project {
    name: string
    reference: string
    thai_abstract: string
    english_abstract: string
    file_url: string
    related: string
    attachments: string
}

// กำหนดตัวแปร projects พร้อม type ที่ชัดเจน
const projects = ref<Project[]>([])

// ฟังก์ชันจำลองการดึงข้อมูลจาก API
const fetchProjects = async () => {
    try {
        // ตัวอย่าง JSON จำลอง
        const data: Project[] = [
            {
                name: "Project A",
                reference: "Reference A",
                thai_abstract: "บทคัดย่อภาษาไทยของโปรเจกต์ A",
                english_abstract: "English abstract for Project A",
                file_url: "https://example.com/files/project-a.pdf",
                related: "Related A",
                attachments: "Attachment A"
            },
            {
                name: "Project B",
                reference: "Reference B",
                thai_abstract: "บทคัดย่อภาษาไทยของโปรเจกต์ B",
                english_abstract: "English abstract for Project B",
                file_url: "https://example.com/files/project-b.pdf",
                related: "Related B",
                attachments: "Attachment B"
            },
            {
                name: "Project A",
                reference: "Reference A",
                thai_abstract: "บทคัดย่อภาษาไทยของโปรเจกต์ A",
                english_abstract: "English abstract for Project A",
                file_url: "https://example.com/files/project-a.pdf",
                related: "Related A",
                attachments: "Attachment A"
            },
            {
                name: "Project A",
                reference: "Reference A",
                thai_abstract: "บทคัดย่อภาษาไทยของโปรเจกต์ A",
                english_abstract: "English abstract for Project A",
                file_url: "https://example.com/files/project-a.pdf",
                related: "Related A",
                attachments: "Attachment A"
            },
            {
                name: "Project A",
                reference: "Reference A",
                thai_abstract: "บทคัดย่อภาษาไทยของโปรเจกต์ A",
                english_abstract: "English abstract for Project A",
                file_url: "https://example.com/files/project-a.pdf",
                related: "Related A",
                attachments: "Attachment A"
            },
            {
                name: "Project A",
                reference: "Reference A",
                thai_abstract: "บทคัดย่อภาษาไทยของโปรเจกต์ A",
                english_abstract: "English abstract for Project A",
                file_url: "https://example.com/files/project-a.pdf",
                related: "Related A",
                attachments: "Attachment A"
            },
            {
                name: "Project A",
                reference: "Reference A",
                thai_abstract: "บทคัดย่อภาษาไทยของโปรเจกต์ A",
                english_abstract: "English abstract for Project A",
                file_url: "https://example.com/files/project-a.pdf",
                related: "Related A",
                attachments: "Attachment A"
            },
            {
                name: "Project A",
                reference: "Reference A",
                thai_abstract: "บทคัดย่อภาษาไทยของโปรเจกต์ A",
                english_abstract: "English abstract for Project A",
                file_url: "https://example.com/files/project-a.pdf",
                related: "Related A",
                attachments: "Attachment A"
            },
            {
                name: "Project A",
                reference: "Reference A",
                thai_abstract: "บทคัดย่อภาษาไทยของโปรเจกต์ A",
                english_abstract: "English abstract for Project A",
                file_url: "https://example.com/files/project-a.pdf",
                related: "Related A",
                attachments: "Attachment A"
            },
        ]
        // กำหนดข้อมูลให้ตัวแปร projects
        projects.value = data
    } catch (error) {
        console.error("Error fetching data:", error)
    }
}

// ดึงข้อมูลเมื่อ component โหลด
onMounted(() => {
    fetchProjects()
})
</script>


<template>
    <div class="container mx-auto p-4">
        <!-- ตรวจสอบว่ามีข้อมูลหรือไม่ -->
        <div v-if="projects.length === 0" class="text-center text-gray-500">
            กำลังโหลดข้อมูล...
        </div>

        <!-- แสดงข้อมูลโปรเจกต์ -->
        <div v-else class="flex flex-col gap-y-4 md:grid md:grid-cols-2 md:gap-4 transition">
            <div v-for="(project, index) in projects" :key="index" class="bg-white p-4 rounded-lg shadow hover:scale-105 transition opacity-85 hover:opacity-100">
                <h3 class="text-xl font-semibold text-black mb-2">
                    {{ project.name }}
                </h3>
                <p class="text-sm text-gray-700">
                    <strong>การอ้างอิง:</strong> {{ project.reference }}
                </p>
                <p class="text-sm text-gray-700">
                    <strong>บทคัดย่อ (ภาษาไทย):</strong> {{ project.thai_abstract }}
                </p>
                <p class="text-sm text-gray-700">
                    <strong>Abstract (English):</strong> {{ project.english_abstract }}
                </p>
                <p class="text-sm text-gray-700">
                    <strong>ไฟล์:</strong>
                    <a :href="project.file_url" target="_blank" class="text-blue-500 underline">
                        ดาวน์โหลด
                    </a>
                </p>
                <p class="text-sm text-gray-700">
                    <strong>ที่เกี่ยวข้อง:</strong> {{ project.related }}
                </p>
                <p class="text-sm text-gray-700">
                    <strong>สิ่งที่แนบมา:</strong> {{ project.attachments }}
                </p>
            </div>
        </div>
    </div>
</template>

<style scoped>
.container {
    max-width: 800px;
}

.bg-gray-100 {
    background-color: #f3f4f6;
}

.shadow {
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.rounded-lg {
    border-radius: 0.5rem;
}

.text-blue-500 {
    color: #3b82f6;
}

.text-gray-500 {
    color: #6b7280;
}

.text-gray-700 {
    color: #374151;
}
</style>
