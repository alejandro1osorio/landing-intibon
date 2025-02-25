<template>
  <div class="parent">
    <div class="div1">Header</div>
    <div class="div2">Subheader</div>
    <div class="div3">
      <img src="../assets/otros/tema1.png" alt="Placeholder Image" class="image" />
    </div>
    <div class="div4">
      <img src="../assets/productos/grupo-productos1.png" alt="Sidebar Image" class="image" />
    </div>
    <div class="div5">
      <img src="../assets/logos-sellos/grupo-sellos.png" alt="Extra Content Image" class="image" />
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
  grid-template-columns: repeat(7, 1fr);
  grid-template-rows: repeat(7, 1fr);
  grid-column-gap: 10px;
  grid-row-gap: 10px;
  width: 100%;
  height: 100vh;
  padding: 10px;
  box-sizing: border-box;
}

.div1 {
  grid-area: 1 / 1 / 2 / 8;
  background-color: #ff5733;
  text-align: center;
  padding: 20px;
  font-weight: bold;
}

.div2 {
  grid-area: 2 / 2 / 3 / 7;
  background-color: #33c3ff;
  text-align: center;
  padding: 20px;
}

.div3 {
  grid-area: 3 / 1 / 8 / 6;
  background-color: #75ff33;
  text-align: center;
  padding: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.div3 .image {
  width: 100%;
  height: 100%;
  object-fit: contain;
}

.div4 {
  grid-area: 4 / 6 / 8 / 8;
  background-color: #ff33a1;
  text-align: center;
  padding: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.div4 .image {
  width: 100%;
  height: 100%;
  object-fit: contain;
}

.div5 {
  grid-area: 3 / 6 / 4 / 8;
  background-color: #ffdb33;
  text-align: center;
  padding: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.div5 .image {
  width: 100%;
  height: 100%;
  object-fit: contain;
}
</style>
