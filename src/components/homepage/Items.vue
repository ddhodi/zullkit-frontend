<script setup>
import { ref } from 'vue'
import ItemsCard from '@/components/ItemsCard.vue'

// DATA REAKTIF menggunakan ref
const items = ref([
    { id: 1, title: "Mobile UI Kit", descript: "Mobile UI Kit", image: "items-1.jpg" },
    { id: 2, title: "Online Doctor Consultation", descript: "Website UI Kit", image: "items-2.jpg" },
    { id: 3, title: "Banking Crypto", descript: "Mobile UI Kit", image: "items-3.jpg" },
]);
</script>

<template>
    <div class="container px-4 mx-auto my-16 md:px-12">
        <h2 class="mb-4 text-xl font-medium md:mb-0 md:text-lg">New Items</h2>
        <div class="flex flex-wrap -mx-1 lg:-mx-4">
            <ItemsCard v-for="item in items" :key="item.id" :id="item.id" :title="item.title" :descript="item.descript"
                :image="item.image" />
        </div>
    </div>
</template>
