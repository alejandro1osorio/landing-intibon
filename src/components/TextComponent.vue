<template>
  <div class="container">
    <h2>
      Para Intibon, el bienestar íntimo es un <br>
      <span class="bold-text">estado de tranquilidad, equilibrio y plenitud</span>
    </h2>
    <p>
      en el que me conozco y <strong>me siento bien porque mi zona íntima está saludable y libre de molestias.</strong> Logrando tener <strong>seguridad y confianza</strong> para relacionarme en intimidad y con los demás.
    </p>
    <div class="underline"></div>
  </div>
</template>

<script>
export default {
  name: "TextComponent",
};
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  padding: 20px;
  /* background-color: #f3f4f6; */
}

h2 {
  font-size: 1.5rem;
  font-weight: 300;
  color: #234F76;
}

.highlight {
  font-weight: 600;
}

.bold-text {
  font-weight: 700;
  color: #0077b6;
}

p {
  font-size: 1rem;
  color: #234F76;
  max-width: 600px;
  margin-top: 10px;
}

.underline {
  width: 200px;
  border-bottom: 2px solid #95D3F8;
  margin-top: 10px;
}
</style>
