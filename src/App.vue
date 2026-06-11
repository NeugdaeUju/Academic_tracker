<script setup>
</script>

<template>
  <header>
    <h1 class="titre">AcademicPlanner</h1>
    <p class="subtitles">This planning is for all students who wants to win!</p>
  </header>
  <main>
    <div class="explications">
      <p>We're sorry, this web app is in building. Please, wait a little bit longer before using it.</p>
      <br />
      <p>To wait, you can see how the app will look!</p>
      <br />
      <br />
      <p>Enjoy !</p>
    </div>

    <div class="images">
      <Transition name="fade" appear>
        <img class='image-vue-1' src="./assets/Desktop-2.png" alt="images de la maquettes du site">
      </Transition>
      <Transition name="fade2" appear>
        <img class="image-vue-2" src="./assets/Desktop-1.jpg" alt="image numéro 2 de la maquette du site">
      </Transition>
      <Transition name="fade3" appear>
        <img class="image-vue-3" src="./assets/Desktop-3.png" alt="image numéro 3 de la maquette du site">
      </Transition>
    </div>
  </main>
</template>

<style scoped>

header{
  /*height : 80px;*/
  border-bottom : 1px solid var(--text-color);
  padding : 20px 80px;
}
.titre {
  color : #977f3f;
  margin-bottom : 12px;
}

main {
  margin: 20px;
  display : flex;
  flex-direction: column;
  align-items: center;
}

.explications {
  text-align: center;
  margin : 150px 0;
}

.images {
  width : 90%;
  display : flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap : 25px;
  margin : 20px;
}

.image-vue-1, .image-vue-2, .image-vue-3 {
  border: 0.5px solid var(--text-color);
  border-radius : 10px;
  width : 100%;
}

.fade-appear-active, .fade-enter-active {
  transition : opacity 2000ms ease;
}

.fade2-appear-active, .fade2-enter-active {
  transition: opacity 2000ms ease;
  transition-delay: 200ms; /* démarre après la première */
}

.fade3-appear-active, .fade3-enter-active {
  transition: opacity 2000ms ease;
  transition-delay: 400ms; /* démarre après la seconde */
}

.fade-appear-from, .fade-enter-from, .fade2-appear-from, .fade2-enter-from, .fade3-appear-from, .fade3-enter-from {
  opacity : 0;
}

.fade-appear-to, .fade-enter-to, .fade2-appear-to, .fade2-enter-to, .fade3-appear-to, .fade3-enter-to {
  opacity : 1;
}

</style>
