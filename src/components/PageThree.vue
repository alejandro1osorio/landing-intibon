<template>
  <div class="page-grid">
    <h1 class="page-title"><strong>Crema</strong> <strong style="border-bottom: 5px solid #008EB4; font-weight: 300;">Vaginal</strong></h1>

    <div class="image-structure">
      <div class="image-container">
        <img src="../assets/productos/producto3.png" alt="Shampoo y Baño Líquido Recién Nacido" style="padding: 0 26px;"/>
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
      activeTab: 'benefits',
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

@media (max-width: 768px) {
  .content-tab, p {
    font-size: 0.9rem;
  }
}
</style>
