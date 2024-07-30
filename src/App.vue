<script setup>
// Import du fichier contenant les informations à afficher
import data from './assets/articles.json'

// Imports des composants
import Header from './components/Header.vue'
import FrontPage from './components/FrontPage.vue'
import ArticleCard from './components/ArticleCard.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <div>
    <Header />

    <main>
      <FrontPage :frontPage="data.frontPage" />

      <div class="container articlesList">
        <ArticleCard v-for="article in data.articlesList" :key="article.id" :article="article" />
      </div>
    </main>

    <Footer />
  </div>
</template>

<style scoped>
main {
  padding: 70px 0;
}
.articlesList {
  margin-top: 100px;
  padding: 0 20px;
  display: flex;
  flex-wrap: wrap;
  gap: 30px;
}
</style>
