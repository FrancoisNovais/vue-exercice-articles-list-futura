<script setup>
import data from './assets/articles.json'
import Header from './components/Header.vue'
import Frontpage from './components/Frontpage.vue'
import Article from './components/Article.vue'
import Footer from './components/Footer.vue'

import { ref } from 'vue'

const articleInfos = ref(data)
const articlesList = ref(data.articlesList)
</script>

<template>
  <Header />
  <main>
    <Frontpage
      :title="data.frontPage.title"
      :teaser="data.frontPage.teaser"
      :articleInfos="articleInfos"
      :category="data.frontPage.category.toUpperCase()"
      :subCategory="data.frontPage.subCategory.toUpperCase()"
    />
    <Article v-for="articles in articlesList" :articles="articles" />
  </main>

  <Footer />
</template>

<style scoped>
main {
  width: 1300px;
  margin: 0 auto;
}
</style>
