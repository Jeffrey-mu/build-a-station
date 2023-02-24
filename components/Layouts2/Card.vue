<template>
  <a :href="'./details/' + id" class="card w-100 mx-a my-10 block">
    <div class="card-img">
      <img :src="imgUrl" :alt="title" />
    </div>
    <div class="card-content">
      <div class="card-header">
        <h2 class="card-title">{{ title }}</h2>
        <div class="card-star">
          <i v-for="n in Math.round(star)" :key="n" class="fa fa-star"></i>
          <i v-for="n in 5 - Math.round(star)" :key="n" class="fa fa-star-o"></i>
        </div>
      </div>
      <p class="card-description">{{ description }}</p>
    </div>
  </a>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'Card',
  props: {
    title: {
      type: String,
      required: true,
    },
    id: {
      type: String,
      required: true,
    },
    star: {
      type: Number,
      required: true,
    },
    imgUrl: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
  },
});
</script>

<style scoped>
.card {
  background-color: #fff;
  border-radius: 10px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  overflow: hidden;
}

.card-img {
  height: 200px;
  overflow: hidden;
}

.card-img img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.card-content {
  padding: 16px;
}

.card-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.card-title {
  margin: 0;
  font-size: 20px;
  font-weight: bold;
}

.card-star {
  color: #f5a623;
  font-size: 16px;
}

.card-description {
  margin-top: 12px;
  font-size: 16px;
  line-height: 1.5;
}
</style>
