<template>
  <div class="screen">
    <br>
    <div class="score">
      <h2>L'ennemie a tiré le chiffre {{ enemyNumber }}</h2>
      <h2>Et moi le {{ yourNumber }}</h2>
    </div>
    <router-link class="buttonlose" to="/">Recommencer</router-link>
    <audio src="/assets/musics/triste.mp3" autoplay/>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: `t'es mort`,
      yourNumber: localStorage.getItem("myNumber"),
      enemyNumber: localStorage.getItem("enemyNumber")
    };
  }
};
</script>

<style scoped>
.screen {
  background-image: url("/assets/pictures/losescreen.png");
  background-size: cover;
}
.buttonlose {
  position: absolute;
  bottom: 0;
  left: 580px;
  color: #083b77;
  text-decoration: none;
  background: #ea7739f3;
  padding: 20px 35px 20px 35px;
  border-radius: 5px;
  font-size: 30px;
  cursor: pointer;
}
h2 {
  color: white;
  font-size: 30px;
}
</style>
