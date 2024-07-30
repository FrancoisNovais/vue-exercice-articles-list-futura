<script setup>
const props = defineProps({
  article: Object
})

const categoriesColors = {
  sciences: ['#be80ff', '#6426ff'],
  sante: ['#ff6b9f', '#ff4e52'],
  planete: ['#9fcb5c', '#069849'],
  maison: ['#fa9761', '#ff5957'],
  tech: ['#49adfa', '#2a3df7']
}
</script>

<template>
  <div class="articleCard">
    <img :src="article.image" :alt="article.title" />

    <p>
      <!-- Utilisation de la méthode JavaScript '.toUpperCase()' pour mettre ces textes en majuscule -->
      <span>{{ article.category.toUpperCase() }}</span
      ><span>{{ article.subCategory.toUpperCase() }}</span>
    </p>

    <h2>{{ article.title }}</h2>

    <p class="date">{{ article.date }}</p>
  </div>
</template>

<style scoped>
.articleCard {
  /* Calcul : la largeur disponible du parent ('100%') moins les espaces qu'il y aura entre chaque carte (3 x 30px => 90px). Le résultat de cette soustraction est divisé par 4 car on veut 4 cartes par ligne */
  width: calc((100% - 90px) / 4);
  height: 480px;
}
img {
  width: 100%;
  height: 350px;
  object-fit: cover;
  margin-bottom: 15px;
}
span {
  font-size: 12px;
}
span:first-child {
  margin-right: 10px;
  font-weight: bold;
  letter-spacing: 0.7px;
  /* Texte avec des couleurs dégradées */
  background: linear-gradient(
    45deg,
    v-bind('categoriesColors[article.category][0]'),
    v-bind('categoriesColors[article.category][1]')
  );
  /* Pour la compatibilité de la couleur dégradée entre les différents navigateurs */
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
span:last-child {
  font-weight: 300;
  letter-spacing: 0.3px;
}
h2 {
  margin: 10px 0;
  font-family: var(--font-title);
  font-size: 14px;
  font-weight: bold;
  line-height: 20px;
}
.date {
  letter-spacing: 0.3px;
  font-weight: 300;
  font-size: 12px;
  color: var(--grey);
}
</style>
