<template>
  <div>
    <Layouts3Card v-for="item in data" :title="item.title" :star="4.5" :id="item.id"
      :imgUrl="'http://47.104.212.164:3000/' + item.picture" :user_name="item.user_name" :description="item.description" />
  </div>
</template>
<script setup>
import index from "@/api/index.json"
const data = ref([])
data.value = index
const show = ref(false)
onMounted(() => {
  show.value = !window.location.pathname.includes('details')
})
</script>
