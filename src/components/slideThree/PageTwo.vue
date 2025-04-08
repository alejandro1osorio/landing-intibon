<template>
  <div class="page-grid">
    <div class="top-line"></div>
    <img src="../../assets/logos-sellos/sello3.png" alt="Decorative Image" class="decorative-image" />
    <h1 class="page-title"><strong>Crema</strong> <strong style="border-bottom: 5px solid #008EB4; font-weight: 300;">Vaginal</strong></h1>

    <p class="additional-text">El clotrimazol es el tratamiento de primera línea para <br> tratar infecciones vaginales causadas por hongos.</p>

    <!-- Nuevo Contenedor de Boxes Arriba de la Imagen -->
    <div class="top-box-container">
      <div class="box" style="width: 280px; height: auto; padding-left: 20px; flex-direction: row-reverse; border-radius: 170px 200px 200px 53px;">
        <img src="../../assets/beneficios-productos/icon11.png" alt="box1" class="box-image" />
          <span class="line" style="transform: rotate(-90deg) translate(-93px, 0px);"></span>
        <p class="box-text"><strong>Único avalado</strong> por la Federación Colombiana de Obstetricia y Ginecología.</p>
      </div>
      <div class="box" style="width: 280px; height: auto; border-radius: 200px 240px 90px 200px;">
        <img src="../../assets/beneficios-productos/icon20.png" alt="box2" class="box-image" />
        <span class="line" style="transform: rotate(-90deg) translate(-93px, 0px);"></span>
        <p class="box-text"><strong>Incluye 3 aplicadores</strong></p>
      </div>
    </div>

    <div class="image-structure">
      <div class="image-container">
        <img src="../../assets/productos/producto3-2.png" alt="Shampoo y Baño Líquido Recién Nacido" style="padding: 50px 0;"/>
      </div>
    </div>

    <!-- Nuevo Contenedor de Boxes -->
    
    <div class="box-container">
      <svg class="curved-line" width="100" height="100" viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg" style="transform: translate(193%, -93%) scale(1.60);">
        <path d="M20 80 V20 H90" stroke="#41bba9" stroke-width="2" fill="transparent"/>
        <circle cx="90" cy="20" r="5" fill="#41bba9" stroke="#9dddd3" stroke-width="2"/>
      </svg>
      <div class="box">
        <img src="../../assets/beneficios-productos/icon13.png" alt="box3" class="box-image" />

        <!-- <span class="line" style="transform: rotate(90deg) translate(-93px, 0px);"></span> -->
        <p class="box-text"><strong>Alivia: <br> Ardor</strong></p>
      </div>
      <div class="box">
        <img src="../../assets/beneficios-productos/icon14.png" alt="box4" class="box-image" />
        <span class="line" style="transform: rotate(90deg) translate(-93px, 0px);"></span>
        <p class="box-text"><strong>Alivia: <br> Picazón</strong></p>
      </div>
      <div class="box">
        <img src="../../assets/beneficios-productos/icon15.png" alt="box5" class="box-image" />
        <span class="line" style="transform: rotate(90deg) translate(-93px, 0px);"></span>
        <p class="box-text"><strong>Alivia: <br> Flujo <br> anormal</strong></p>
      </div>
      <div class="box">
        <img src="../../assets/beneficios-productos/icon16.png" alt="box6" class="box-image" />
        <!-- <span class="line" style="transform: rotate(90deg) translate(-93px, 0px);"></span> -->
        <p class="box-text"><strong>Alivia: <br> Mal olor</strong></p>
      </div>
      <svg class="" width="100" height="100" viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg" style="transform: translate(-293%, -96%) scale(1.6);">
        <path d="M80 80 V20 H70" stroke="#41bba9" stroke-width="2" fill="transparent"/>
        <circle cx="70" cy="20" r="5" fill="#41bba9" stroke="#9dddd3" stroke-width="2"/>
      </svg>
    </div>

    <div class="button-group">
      <button @click="setActiveTab('benefits')">Beneficios</button>
      <button @click="setActiveTab('usage')">Modo de uso</button>
      <button @click="setActiveTab('composition')">Composición</button>
    </div>
    <div v-if="activeTab" class="content-tab">
      <div class="tab-header">
        <button class="close-btn" @click="closeTab">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M6 18L18 6M6 6L18 18" stroke="#5d75b8" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </button>
      </div>

      <p v-if="activeTab === 'benefits'" class="text-tab">
        Elimina la infección vaginal causada por hongos.
      </p>
      <p v-if="activeTab === 'usage'">
        Aplicar una carga del dispositivo intravaginal (5 g) una vez al día preferiblemente por la noche antes de acostarse, durante 3 días consecutivos. La crema debe ser introducida profundamente en la vagina.
      </p>
      <p v-if="activeTab === 'composition'">Clotrimazol 2%</p>
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
      activeTab: '',
    };
  },
  methods: {
    setActiveTab(tab) {
      this.activeTab = tab;
    },
    closeTab() {
      this.activeTab = '';
    }
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

.top-line {
  width: 15%;
  height: 2px;
  background-color: #0077b6;
  position: absolute;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
}

.page-title {
  font-size: 1.8rem;
  font-weight: 300;
  text-align: center;
  color: #214F79;
}

.decorative-image {
  position: absolute;
  top: 10px;
  right: 10px;
  width: 100px;
  height: auto;
}

.additional-text {
  text-align: center;
  font-size: 1rem;
  color: #214F79;
  margin: 20px 20px;
  max-width: 80%;
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
  max-width: 600px; /* 100% */
  height: auto;
  border-radius: 10px;
}

/* Estilos para el nuevo contenedor de boxes */
.box-container {
  display: flex;
  flex-direction: row;
  justify-content: center;
  gap: 45px; /* 15px */
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

.line {
  position: absolute;
  width: 94px;
  height: 2px;
  background-color: #41BBA9;
  /* top: 50%;
  transform: translateY(-50%); */
}

.line::after {
  content: '';
  position: absolute;
  width: 20px;
  height: 20px;
  background-color: #41BBA9;
  border: 2px solid #9dddd3;
  border-radius: 50%;
  top: 50%;
  transform: translateY(-50%);
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
  margin-top: 20px;
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

.tab-header {
  display: flex;
  justify-content: flex-end;
  padding: 5px;
}
.close-btn {
  background: transparent;
  border: none;
  font-size: 1.5rem;
  cursor: pointer;
  color: #E4016A;
}

footer {
  background: #EEAF00;
  font-size: 1.5rem;
  width: 100%;
  margin-top: 30px;
  display: flex;
  align-items: center;
  justify-content: center;
  visibility: hidden; /* footer oculto */
}

.text-footer {
  color: #fff;
}

@media (max-width: 768px) {
  .page-grid {
    justify-content: center;
  }

  .additional-text {
    font-size: 0.9rem;
    max-width: 90%;
  }

  .decorative-image {
    display: none;
  }

  .box {
    visibility: hidden;
  }

  .image-container img {
    max-width: 350px;
  }
}
</style>