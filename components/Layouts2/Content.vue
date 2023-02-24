<template>
  <div v-if="show">
    <Layouts2Card v-for="item in data" :title="item.title" :star="4.5"
    :id="item.id"
    :imgUrl="'http://47.104.212.164:3000/' + item.picture"
      :description="item.description" />
  </div>

  <Layouts2Details :item="item" v-else />
</template>
<script setup>
import index from "@/api/index.json"
const data = ref([])
const item = ref({})
data.value = index
const show = ref(false)
onMounted(() => {
  show.value = !window.location.pathname.includes('details')
  item.value = index.find(el => el.id == window.location.pathname.split('/').at(-1))
})
</script>
