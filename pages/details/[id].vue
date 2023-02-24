<script setup>
import { layout } from "@/config/layout"
import index from "@/api/index.json"
const route = useRoute()
definePageMeta({
  layout: layout,
})
const data = ref([])
const item = ref({})
const show = ref(false)
onMounted(() => {
  show.value = !window.location.pathname.includes('details')
  item.value = index.find(el => el.id == route.params.id)
})
</script>


<template>
  <div>
    <Layouts3Details :item="item"/>
  </div>
</template>
