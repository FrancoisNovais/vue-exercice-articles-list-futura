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
      <div>
        <div class="category-bloc">
          <p>
            <span class="linear-text-gradient">{{ category }}</span>
          </p>
          <p>{{ subCategory }}</p>
        </div>
        <div>
          <span class="title">
            {{ title }}
          </span>
        </div>
      </div>

      <p class="teaser">
        {{ teaser }}
      </p>
    </div>
  </section>
</template>

<style scoped>
section {
  margin: 20px 0;
  height: 550px;
  position: relative;
}
section > div {
  position: absolute;
  top: 80px;
  left: 80px;
  max-width: 800px;
}
section > div > div:first-child {
  border-left: 4px solid;
  border-image: linear-gradient(to bottom, #be80ff, #6325ff) 1;
}
.category-bloc {
  display: flex;
  background-color: black;
  color: white;
  padding: 8px 8px 5px 0;
  width: fit-content;
}

span {
  padding: 5px;
}
.title {
  font-family: 'Merriweather', serif;
  font-style: italic;
  font-size: 34px;
  background-color: black;
  line-height: 50px;
  color: white;
}

.teaser {
  background-color: rgba(0, 0, 0, 0.5);
  color: white;
  margin: 2.5rem 0 0;
  padding: 1.5rem;
  line-height: 20px;
}
img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: bottom;
  position: relative;
}
.linear-text-gradient {
  background: linear-gradient(to right, #be80ff, #6325ff);
  background-clip: text;
  color: transparent;
}
</style>
