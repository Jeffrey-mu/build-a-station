<script setup lang="ts">
defineProps<{ item: any }>()
</script>
<template>
  <div class="container">
    <div class="title">
      <h1 class="text-3xl">{{ item.title }}</h1>
      <h2 class="text-2xl">{{ item.subtitle }}</h2>
    </div>
    <div class="metadata">
      <p>By {{ item.user_name }} on {{ item.time }}</p>
    </div>
    <div class="content">
      <div v-html="item.content"></div>
    </div>
    <div class="keywords">
      <p>Keywords: {{ item.keywords }}</p>
    </div>
  </div>
</template>
<style>
.container {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}

.title {
  text-align: center;
  margin-bottom: 20px;
}

.metadata {
  text-align: right;
  margin-bottom: 20px;
}

.keywords {
  margin-top: 20px;
  text-align: center;
  font-style: italic;
}

.keywords p {
  margin: 0;
}

.content h1 {
  font-size: 32px;
  margin-top: 30px;
}

.content h2 {
  font-size: 28px;
  margin-top: 25px;
}

.content p {
  font-size: 18px;
  line-height: 1.5;
  margin-top: 20px;
  text-align: justify;
}

.content ul {
  font-size: 18px;
  line-height: 1.5;
  margin-top: 20px;
  margin-left: 30px;
}

.content ul li {
  margin-bottom: 10px;
}

.content img {
  max-width: 100%;
  height: auto;
  margin-top: 20px;
}
</style>
