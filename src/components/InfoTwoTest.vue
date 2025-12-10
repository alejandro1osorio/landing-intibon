<template>
  <div class="parent" id="50color">
    <div class="div1">
      <div class="title-wrapper">
        <h1 class="title">
          Intibon <strong style="border-bottom: 5px solid #008EB4;">45+</strong>
        </h1>
        <p class="subtitle">
          Cuidado íntimo especializado para acompañar los cambios
          naturales de tu cuerpo después de los 45 años.
        </p>
      </div>
    </div>
    <div class="div2">
      <img src="../assets/otros/tema2.png" alt="Placeholder Image" class="image" />
    </div>
    <div class="div3">
      <img src="../assets/productos/grupo-produtos22.png" alt="Placeholder Image" class="image-centered" />
    </div>
  </div>
</template>

<script>
export default {
  name: "GridLayout"
};
</script>

<style scoped>
.parent {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  grid-template-rows: repeat(5, 1fr);
  grid-column-gap: 0px;
  grid-row-gap: 0px;
  width: 100%;
  height: 100vh;
  padding: 0;
  box-sizing: border-box;
}

.div1 {
  grid-area: 1 / 1 / 2 / 13;  /* 1, 2, 2, 11 */ 
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  margin: 0;
  position: relative;
  text-align: center;
}

.title-wrapper {
  max-width: 700px;
  padding: 0 16px;
}

.top-line {
  width: 15%;
  height: 2px;
  background-color: orange;
  position: absolute;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
}

.div1 .title {
  font-size: 2em;
  font-weight: 300;
  color: #214F79;
  margin-bottom: 0.4em;
}

.subtitle {
  font-size: 1rem;
  line-height: 1.4;
  color: #4b678a;
  margin: 0 auto;
  /* Mantener visualmente en 2 líneas máximo */
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  overflow: hidden;
}

.div2 {
  grid-area: 2 / 1 / 6 / 8;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
  margin: 0;
}

.div2 .image {
  width: 100%;
  height: 100%;
  object-fit: contain;
}

.div3 {
  grid-area: 2 / 9 / 5 / 12;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.5em;
  height: 100%;
  margin: 0;
}

.div3 .image-centered {
  max-width: 100%;
  max-height: 100%;
  object-fit: contain;
}

/* Ya no existe div4 */

/* Responsivo */
@media screen and (min-width: 1400px) {
  /* Estilos para monitores muy grandes */
  .div1 .title {
    font-size: 2.4em;
  }
  .subtitle {
    font-size: 1.05rem;
  }
}

@media screen and (min-width: 1024px) and (max-width: 1399px) {
  /* portátiles con pantallas medianas */
  .div1 .title {
    font-size: 2.1em;
  }
}

@media screen and (max-width: 768px) {
  .parent {
    grid-template-columns: repeat(6, 1fr);
    grid-template-rows: auto;
    height: 110vh;
  }

  .div1 {
    grid-area: 1 / 1 / 2 / 7;
  }

  .div1 .title {
    font-size: 1.5em;
  }

  .subtitle {
    font-size: 0.95rem;
  }

  .div2 {
    grid-area: 2 / 1 / 3 / 7;
  }

  .div3 {
    grid-area: 3 / 1 / 4 / 7;
  }

  .top-line {
    width: 190px;
  }

  .div3 .image-centered {
    max-width: 93%;
  }
}
</style>
