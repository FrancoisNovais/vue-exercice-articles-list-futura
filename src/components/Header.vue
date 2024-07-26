<script setup></script>

<template>
  <header>
    <h1>Futura</h1>
    <ul>
      <li>Sciences <font-awesome-icon :icon="['fas', 'chevron-down']" /></li>
      <li>Sante <font-awesome-icon :icon="['fas', 'chevron-down']" /></li>
      <li>Tech <font-awesome-icon :icon="['fas', 'chevron-down']" /></li>
      <li>Maison <font-awesome-icon :icon="['fas', 'chevron-down']" /></li>
      <li>Planete <font-awesome-icon :icon="['fas', 'chevron-down']" /></li>
    </ul>
    <button>Je m'abonne</button>
  </header>
</template>

<style scoped>
header {
  /* border: 2px solid red; */
  padding: 10px 20px;
  background: linear-gradient(to right, #be80ff, #6325ff);
  display: flex;
  justify-content: space-between;
  align-items: center;
}
ul {
  display: flex;
  gap: 20px;
  color: white;
  text-transform: uppercase;
}
li {
  cursor: pointer;
}
svg {
  margin-left: 5px;
  font-size: 12px;
}
button {
  background-color: #ffaf15;
  color: white;
  border: none;
  padding: 10px 15px;
  text-transform: uppercase;
  cursor: pointer;
  font-weight: bold;
}
button:hover {
  background-color: #d28a4e;
}
</style>
