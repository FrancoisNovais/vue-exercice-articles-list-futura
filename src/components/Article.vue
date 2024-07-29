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
      <div>
        <p>
          <span class="linear-text-gradient">{{ articles.category }}</span>
        </p>
        <p>{{ articles.subCategory }}</p>
      </div>
      <h2>
        {{ articles.title }}
      </h2>

      <p class="date">{{ articles.date }}</p>
    </div>
  </section>
</template>

<style scoped>
section {
  width: calc((100% / 4) - 30px);
  height: 480px;
  display: flex;
  flex-direction: column;
  position: relative;
}
section > div {
  height: 30%;
}
section > div > div {
  display: flex;
  margin: 10px 0;
  text-transform: uppercase;
  font-size: 14px;
}

h2 {
  margin-bottom: 10px;
  font-weight: bold;
}
span {
  margin-right: 10px;

  font-weight: bold;
}
img {
  height: 100%;
  object-fit: cover;
  object-position: bottom;
}
.date {
  font-size: 14px;
}
.linear-text-gradient {
  background: linear-gradient(to right, #be80ff, #6325ff);
  background-clip: text;
  color: transparent;
}
</style>
