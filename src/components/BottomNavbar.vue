<template>
  <nav>
    <div class="button-container">
      <div class="add-button">+</div>
    </div>
    <section class="main-tabs">
      <ul class="tabs-container-mobile">
        <li class="tab-option-mobile">Resumen</li>
        <li class="tab-option-mobile">Cuentas</li>
        <li class="tab-option-mobile">Ingresos</li>
        <li class="tab-option-mobile">Gastos</li>
      </ul>
    </section>
  </nav>
</template>

<script>
export default {
  name: "BottomNavbar"
};
</script>

<style>
nav {
  display: none;
  position: fixed;
  border-radius: 15px 15px 0 0;
  background: #6cb2eb;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 70px;
}

.button-container {
  position: relative;
}

.add-button {
  position: absolute;
  left: 50%;
  top: -25px;
  cursor: pointer;
  box-shadow: 0px 5px 20px 0px rgba(28, 61, 90, 1);
  transform: translateX(-50%);
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  font-size: 1.5rem;
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background: #2779bd;
}

.tabs-container-mobile {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  list-style: none;
  padding: 0;
  margin: 0;
  font-weight: 500;
  color: #eff8ff;
  justify-content: space-around;
}
.tab-option-mobile {
  height: 100%;
  padding-top: 30px;
}

.main-tabs,
.tabs-container-mobile,
.tab-option-mobile {
  height: 100%;
}

@media (max-width: 1024px) {
  nav {
    display: initial;
  }
}
</style>