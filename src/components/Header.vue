<script setup>
import { ref } from 'vue'

const activeItem = ref(0)
</script>

<template>
  <header>
    <div class="app-block">
      <img class='logo' src="../assets/logo.svg"/>
      <div class="texts">
        <img class='nom-app' src="../assets/nom-logo.svg">
        <p class="parcours-list">L3 → M1 → M2</p>
      </div>
    </div>

    <nav>
      <h2 class="titre-section">FORMATIONS</h2>
      <ul class="liste-nav">
        <li class="item color1" :class="{ active : activeItem === 0}" @click="activeItem = 0"><div class="mark"></div>L3 Gestion FAD</li>
        <li class="item color2" :class="{ active : activeItem === 1}" @click="activeItem = 1"><div class="mark"></div>M1 PME & Entrepr.</li>
        <li class="item color3" :class="{ active : activeItem === 2}" @click="activeItem = 2"><div class="mark"></div>M2 MAE</li>
      </ul>
    </nav>

    <div class="progession-block">
      <div class="titre-prct">
        <p class="titre-section">Progression globale</p>
        <span class="pourcentage">18%</span>
      </div>
      <div class="progress-bar">
        <div class="progress-bar-empty"></div>
        <div class="progress-bar-color"></div>
      </div>
    </div>
    
  </header>
</template>

<style scoped>

header {
  Width : 300px;
  height : 100vh;
  position : relative;
  top : 0;
  left: 0;
  background: var(--bg-color);
  /*padding : 0 24px;*/
}

/* Block Nom général*/
.app-block {
  display : flex;
  align-items: center;
  gap : 8px;
  padding : 37px 24px;
  border-bottom : 1px solid var(--text-color)
}

.logo {
  width : 55px;
  height : 100%;
}

.nom-app {
  width : 184px;
  height : 1001%;
}

.parcours-list {
  margin-left : 8px;
  color : var(--grey1);
  font-weight : medium;
  font-size : 12px;
}

/* Navigation */

nav {
  padding : 15px 0;
}

li::marker {
  content : none;
}

.titre-section {
  font-size : 8px;
  font-family : 'work sans', sans-serif;
  color : var(--grey1);
  margin-bottom : 15px;
  letter-spacing: 1.75%;
  font-weight : 600;
  margin-left : 24px;
}

.item {
  font-size : 11px;
  color : var(--grey2);
  padding : 15px;
  display : flex;
  flex-direction: row;
  cursor: pointer;
}

.mark {
  width : 14px;
  height : 14px;
  border-radius: 999px;
  margin-left : 28px;
  margin-right : 20px;
}

.item:nth-child(1) .mark {
  background-color: var(--violet);
}

.item:nth-child(2) .mark {
  background-color: var(--vert);
}

.item:nth-child(3) .mark {
  background-color: var(--orange);
}

.active.color1 {
  background-color: #EEEDFE;
  border-left : 3px solid var(--violet);
}

.active.color2 {
  background-color: #DBEFCA;
  border-left : 3px solid var(--vert);
}

.active.color3 {
  background-color: #EAD5B7;
  border-left : 3px solid var(--orange);
}

/* Block progression globale */

.progession-block {
  position : absolute ;
  bottom :0;
  border-top : 1px solid var(--text-color);
  padding-top : 15px;
  font-size : 10px;
}

.pourcentage {
  color : var(--grey1);
  font-size : 10px;
  margin-bottom : 15px;
  margin-right : 24px;
}

.titre-prct {
  display : flex;
  justify-content: space-between;
  align-items: center;
}

.titre-prct .titre-section {
  font-size : 10px;
}

.progress-bar {
  width: 280px;
  margin : 7px 10px 53px 10px;
  position : relative;
}

.progress-bar-empty {
  position : absolute ;
  height : 4px;
  width: 100%;
  background-color : #fff;
  border-radius: 999px;
}

.progress-bar-color {
  position : absolute;
  background: var(--violet);
  height : 4px;
  width: 18%;
  border-radius: 999px;

}

</style>
