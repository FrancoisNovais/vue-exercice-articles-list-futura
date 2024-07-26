<script setup>
const props = defineProps({
  title: String,
  teaser: String,
  image: String,
  category: String,
  subCategory: String,
  articleInfos: Object
})
</script>

<template>
  <section>
    <img :src="articleInfos.frontPage.image" />
    <div>
      <p>
        <span>{{ category }}</span>
      </p>
      <p>{{ subCategory }}</p>

      <h2>
        {{ title }}
      </h2>
    </div>

    <p>
      {{ teaser }}
    </p>
  </section>
</template>

<style scoped>
section {
  border: 2px solid greenyellow;
  margin: 20px;
}
img {
  width: 500px;
}
</style>
