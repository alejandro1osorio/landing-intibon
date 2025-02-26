<template>
  <div class="container">
    <h2>
      Para Intibon, el bienestar íntimo es un <br>
      <span class="bold-text">estado de tranquilidad, equilibrio y plenitud</span>
    </h2>
    <p>
      Cuando la zona íntima de la mujer está saludable y libre de molestias, se conoce y se siente el verdadero bienestar. Logrando tener seguridad y confianza para relacionarse en intimidad y con los demás.
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
  border-bottom: 2px solid #0077b6;
  margin-top: 10px;
}
</style>
