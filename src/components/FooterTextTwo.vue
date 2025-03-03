<template>
  <div class="footer-text">
    <p>2. Mark JKK, SamsudinS, LooiI, YuenKH. Vaginal dryness: a reviewofcurrent understandingand managementstrategies. Climacteric. Junio de 2024;27(3):236-244.</p>
  </div>
</template>

<script>
export default {
  name: "FooterText",
};
</script>

<style scoped>
.footer-text {
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  font-size: 0.9em;
  line-height: 1;
  color: #666b70;
  padding: 0 20px;
  font-style: italic;
  /* background-color: rgba(255, 255, 255, 0.8); */
  width: 100%;
  max-width: 100%;
  overflow: hidden;
}

@media screen and (max-width: 768px) { 
  .footer-text {
    font-size: 7px;
    padding: 0px 0px;
  }
}

@media (min-width: 1024px) and (max-width: 1366px) {
  .footer-text {
    padding: 10px;
  }

  p {
    font-size: 0.75em;
    line-height: 1.4;
    text-align: left; /* En móviles, mejor alineado a la izquierda */
  }
}

</style>