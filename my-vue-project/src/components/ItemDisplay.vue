<template>
  <div class="item">
    <img :src="image" alt="Item Image" class="item-image" />
    <div class="item-content">
      <p>{{ title }}</p>
      <span>{{ date }}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ItemDisplay',
  props: {
    title: String,
    date: String,
    image: String
  }
}
</script>

<style scoped>
.item {
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  overflow: hidden;
}
.item-image {
  width: 100%;
  height: auto;
}
.item-content {
  padding: 10px;
}
</style>
