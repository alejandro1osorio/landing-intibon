<template>
  <div class="page-grid">
    <h1 class="page-title"><strong>Crema</strong> <strong style="border-bottom: 5px solid #008EB4; font-weight: 300;">Vaginal</strong></h1>

    <!-- Nuevo Contenedor de Boxes Arriba de la Imagen -->
    <div class="top-box-container">
      <div class="box" style="width: 280px; height: auto; padding-left: 20px; flex-direction: row-reverse; border-radius: 170px 200px 200px 53px;">
        <img src="../assets/beneficios-productos/icon11.png" alt="box1" class="box-image" />
        <p class="box-text"><strong>Único avalado</strong> por la Federación Colombiana de Obstetricia y Ginecología.</p>
      </div>
      <div class="box" style="width: 280px; height: auto; border-radius: 200px 240px 90px 200px;">
        <img src="../assets/beneficios-productos/icon12.png" alt="box2" class="box-image" />
        <p class="box-text"><strong>Incluye 3 aplicadores</strong></p>
      </div>
    </div>

    <div class="image-structure">
      <div class="image-container">
        <img src="../assets/productos/producto3.png" alt="Shampoo y Baño Líquido Recién Nacido" style="padding: 0 26px;"/>
      </div>
    </div>

    <!-- Nuevo Contenedor de Boxes -->
    <div class="box-container">
      <div class="box">
        <img src="../assets/beneficios-productos/icon13.png" alt="box3" class="box-image" />
        <p class="box-text"><strong>Alivia: <br> Ardor</strong></p>
      </div>
      <div class="box">
        <img src="../assets/beneficios-productos/icon14.png" alt="box4" class="box-image" />
        <p class="box-text"><strong>Alivia: <br> Picazón</strong></p>
      </div>
      <div class="box">
        <img src="../assets/beneficios-productos/icon15.png" alt="box5" class="box-image" />
        <p class="box-text"><strong>Alivia: <br> Flujo <br> anormal</strong></p>
      </div>
      <div class="box">
        <img src="../assets/beneficios-productos/icon16.png" alt="box6" class="box-image" />
        <p class="box-text"><strong>Alivia: <br> Mal olor</strong></p>
      </div>
    </div>

    <div class="button-group">
      <button @click="setActiveTab('benefits')">Beneficios</button>
      <button @click="setActiveTab('usage')">Modo de uso</button>
      <button @click="setActiveTab('composition')">Composición</button>
    </div>
    <div class="content-tab">
      <p v-if="activeTab === 'benefits'" class="text-tab">
        INTIBON® 45+ Gel Hidratante íntimo que contiene ácido hialurónico, Vitamina E y un complejo hidratante, ayudan a brindar un efecto de hidratación y sensación de bienestar en tu zona íntima externa. <strong>No altera el pH fisiológico de la zona y no mancha la ropa interior.</strong>
      </p>
      <p v-if="activeTab === 'usage'">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Veritatis, dignissimos.</p>
      <p v-if="activeTab === 'composition'">Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque, obcaecati?</p>
    </div>

    <footer>
      <p class="text-footer">Desarrollado con <strong>Ginecólogos Expertos.</strong></p>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'PageOne',
  data() {
    return {
      activeTab: 'benefits'
    };
  },
  methods: {
    setActiveTab(tab) {
      this.activeTab = tab;
    },
  },
};
</script>

<style scoped>
.page-grid {
  display: grid;
  grid-template-rows: auto 1fr;
  justify-items: center;
  align-items: center;
  width: 100%;
  height: 100%;
  box-sizing: border-box;
}

.page-title {
  font-size: 1.8rem;
  font-weight: 300;
  text-align: center;
  color: #214F79;
}

/* Estilos para el contenedor superior de cajas */
.top-box-container {
  display: flex;
  justify-content: center;
  gap: 15px;
  width: 100%;
  margin-bottom: 20px;
}


.image-structure {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
}

.image-container {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 130%;
  max-width: 300px;
}

.image-container img {
  max-width: 100%;
  height: auto;
  border-radius: 10px;
}

/* Estilos para el nuevo contenedor de boxes */
.box-container {
  display: flex;
  flex-direction: row;
  justify-content: center;
  gap: 15px;
  width: 100%;
  margin-top: 20px;
}

.box {
  display: flex;
  align-items: center;
  gap: 10px;
  background: #ffffff;
  /* padding: 10px; */
  border-radius: 200px 77px 230px 200px;
  width: 200px;
  height: auto;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.box-image {
  width: 100px;
  height: auto;
}

.box-text {
  font-weight: 400;
  color: #214F79;
  font-size: 0.8rem;
}

.content-tab {
  border: 2px solid #EEAF00;
  border-radius: 0px 12px 12px 12px;
  width: 60%;
  padding: 20px;
  background: #F3F3F3;
}

.content-tab, p {
  font-weight: 400;
  color: #214F79;
}

.button-group {
  display: flex;
  gap: 10px;
}

button {
  padding: 5px 10px;
  font-size: 0.9rem;
  border: none;
  border-radius: 5px;
  background-color: #DEE5E7;
  color: #214F79;
  cursor: pointer;
  transition: background-color 0.3s;
}

button:hover {
  color: white;
  background-color: #EEAF00;
}

button:active,
button:focus {
  background-color: #EEAF00;
  color: #fff;
}

footer {
  background: #EEAF00;
  font-size: 1.5rem;
  width: 100%;
  margin-top: 30px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.text-footer {
  color: #fff;
}
</style>