<template>
  <header>
    <img src="../assets/logo.svg" alt="" />

    <nav>
      <p>SCIENCES <font-awesome-icon :icon="['fas', 'angle-down']" /></p>
      <p>SANTE <font-awesome-icon :icon="['fas', 'angle-down']" /></p>
      <p>TECH <font-awesome-icon :icon="['fas', 'angle-down']" /></p>
      <p>MAISON <font-awesome-icon :icon="['fas', 'angle-down']" /></p>
      <p>PLANETE <font-awesome-icon :icon="['fas', 'angle-down']" /></p>
    </nav>

    <button>JE M'ABONNE</button>
  </header>
</template>

<style scoped>
header {
  height: 60px;
  padding: 0 55px;
  color: white;
  display: flex;
  align-items: center;
  justify-content: space-between;
  /* Pour obtenir un arrière plan avec des couleurs dégradées */
  background: linear-gradient(45deg, var(--light-purple), var(--dark-purple));
}
nav {
  display: flex;
  gap: 25px;
}
svg {
  margin-left: 5px;
}
button {
  background-color: var(--yellow);
  padding: 10px 15px;
  font-size: 14px;
  border: none;
  /* Pour dire au bouton de prendre la couleur de texte, la police de caractère et la taille de caractère de son parent */
  color: inherit;
  font-family: inherit;
  font-size: inherit;
}
</style>
