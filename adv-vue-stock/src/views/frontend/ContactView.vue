<template>
    <section class="container px-4 py-12 mx-auto sm:py-16 md:py-20 xl:py-28">
        <div class="mb-10 space-y-4 text-center lg:mb-16">
            <h2 class="text-4xl font-semibold md:text-5xl">Contact us</h2>
            <p class="mx-auto text-lg md:max-w-md">ติดต่อเรา</p>
        </div>
        <div class="grid gap-6 md:grid-cols-2 xl:grid-cols-2 lg:gap-10">
            <div class="p-8 transition-colors duration-200 border-2 border-gray-200 rounded-lg hover:border-emerald-600">
                <div class="grid md:grid-cols-2">
                    <h1 class="font-bold mb-4">ที่อยู่</h1>
                    <p class="text-end"></p>
                </div>
                <p class="mb-4">789 หมู่ 4 ถ.มิตรภาพ ต.จอหอ อ.เมือง จ.นครราชสีมา 30000</p>
                <p>โทร.02-123-7894</p>
                <p>อีเมล์ contactpook@gmail.com</p>
            </div>
            <div class="p-8 transition-colors duration-200 border-2 border-gray-200 rounded-lg hover:border-emerald-600">
                <div class="grid md:grid-cols-2">
                    <h1 class="font-bold mb-4">ข้อมูลการชำระเงิน</h1>
                    <p class="text-end">
                        <button @click="copy()">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6 inline-block text-emerald-600">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M9 12h3.75M9 15h3.75M9 18h3.75m3 .75H18a2.25 2.25 0 002.25-2.25V6.108c0-1.135-.845-2.098-1.976-2.192a48.424 48.424 0 00-1.123-.08m-5.801 0c-.065.21-.1.433-.1.664 0 .414.336.75.75.75h4.5a.75.75 0 00.75-.75 2.25 2.25 0 00-.1-.664m-5.8 0A2.251 2.251 0 0113.5 2.25H15c1.012 0 1.867.668 2.15 1.586m-5.8 0c-.376.023-.75.05-1.124.08C9.095 4.01 8.25 4.973 8.25 6.108V8.25m0 0H4.875c-.621 0-1.125.504-1.125 1.125v11.25c0 .621.504 1.125 1.125 1.125h9.75c.621 0 1.125-.504 1.125-1.125V9.375c0-.621-.504-1.125-1.125-1.125H8.25zM6.75 12h.008v.008H6.75V12zm0 3h.008v.008H6.75V15zm0 3h.008v.008H6.75V18z" />
                            </svg>
                            {{ copied ? 'คัดลอกแล้ว':'คัดลอกเลขบัญชี' }}
                        </button>
                    </p>
                </div>
                <p>ธนาคารกรุงไทย</p>
                <p>เลขบัญชี: <span>741-8522-963</span></p>
                <p>สาขาจอหอ</p>
                <p>บัญชีประเภท: ออมทรัพย์</p>
                <p>ชื่อบัญชี: Woraprat Charoenmueangphiaw</p>
            </div>
        </div>
    </section>
</template>

<script setup lang="ts">
    
    import { ref } from 'vue'
    import { useClipboard } from '@vueuse/core'

    const accNumber = ref('0104349835')
    const { copy, copied } = useClipboard({ source: accNumber.value, copiedDuring: 2000 })

</script>

<style scoped>

</style>