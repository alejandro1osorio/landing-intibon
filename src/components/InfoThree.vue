<template>
  <div class="parent" id="tratamiento">
    <div class="div1">
      <h1 class="title"><strong>Plataforma de Tratam<strong style="border-bottom: 5px solid #008EB4;">iento</strong></strong></h1>
      <p class="description">Alrededor del 80 a 90% de casos de candidiasis vulvovaginal sintomática son de <strong style="color: #008FB2;">naturaleza no <br> complicada</strong> y de estos entre el 75 al 90% se producen por el crecimiento excesivo de C.albicans.</p>
    </div>
    <div class="div2">
      <img src="../assets/otros/tema3.png" alt="Placeholder Image" class="image" />
    </div>
    <div class="div4">
      <img src="../assets/logos-sellos/sello3.png" alt="Placeholder Image" class="image-centered" />
    </div>
    <div class="div3">
      <img src="../assets/productos/grupo-productos3.png" alt="Placeholder Image" class="image-centered" />
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
  grid-area: 1 / 1 / 2 / 13;
  color: white;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  margin: 0;
  position: relative;
  text-align: center;
}

.div1 .title {
  font-size: 2em;
  font-weight: 300;
  color: #214F79;
}

.div1 .description {
  font-size: 1em;
  color: #214F79;
  margin-top: 10px;
  text-align: center;
  max-width: 80%;
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

.div4 {
  grid-area: 2 / 9 / 3 / 12;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.5em;
  height: 80px;
  margin: 0;
}

.div4 .image-centered {
  max-width: 140%;
  max-height: 140%;
  object-fit: contain;
}

.div3 {
  grid-area: 3 / 9 / 5 / 12;
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

@media screen and (min-width: 1400px) {
  .div4 {
    height: 190px;
  }

  .div4 .image-centered {
    max-width: 120%;
    max-width: 120%;
  }

  .div3 {
    height: 117%;
  }
}

@media screen and (min-width: 1024px) and (max-width: 1399px) {
  .div4 {
    height: 90px;
  }

  .div4 .image-centered {
    max-width: 116%;
    max-height: 116%;
  }

  .div3 {
    height: 133%;
  }
}

@media screen and (max-width: 768px) {
  .parent {
    grid-template-columns: repeat(6, 1fr);
    grid-template-rows: auto;
    height: 140vh;
  }

  .div1 {
    grid-area: 1 / 1 / 2 / 7;
  }

  .div1 .title {
    font-size: 1.5em;
  }

  .div2 {
    grid-area: 2 / 1 / 3 / 7;
  }

  .div4 {
    grid-area: 3 / 1 / 4 / 7;
  }

  .div4 .image-centered {
    max-width: 100%;
    max-height: 100%;
  }

  .div3 {
    grid-area: 4 / 1 / 5 / 7;
  }

  .div3 .image-centered {
    max-width: 90%;
  }
}
</style>
