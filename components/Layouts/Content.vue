<template>
  <div v-if="show" flex="~ wrap">
    <LayoutsCard v-for="item in data" :title="item.title" :star="4.5" :id="item.id"
      :imgUrl="'http://47.104.212.164:3000/' + item.picture" :description="item.description" />
  </div>

  <LayoutsDetails :item="item" v-else v-if="item"/>
</template>
<script setup>
import index from "@/api/index.json"
const data = ref([])
const item = ref(null)
data.value = index
const show = ref(false)
onMounted(() => {
  show.value = !window.location.pathname.includes('details')
  item.value = index.find(el => el.id == window.location.pathname.split('/').at(-1))
})
</script>
