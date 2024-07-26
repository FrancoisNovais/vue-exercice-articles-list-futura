<script setup>
// Déclarer les props
const props = defineProps({
  articles: Object
})
</script>

<template>
  <section>
    <img :src="articles.image" />
    <div>
      <p>
        <span>{{ articles.category }}</span>
      </p>
      <p>{{ articles.subCategory }}</p>
    </div>
    <h2>
      {{ articles.title }}
    </h2>

    <p>{{ articles.date }}</p>
  </section>
</template>

<style scoped>
section {
  border: 2px solid blue;
  margin: 20px;
}
img {
  width: 500px;
}
</style>
