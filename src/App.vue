<template>
  <div id="app">
    <section class="desktop-layout">
      <div class="left-navbar">
        <ul class="tabs-container">
          <li class="tab-option">Resumen</li>
          <li class="tab-option">Cuentas</li>
          <li class="tab-option">Ingresos</li>
          <li class="tab-option">Gastos</li>
        </ul>
      </div>
      <div class="main-content">
        <img alt="Vue logo" src="./assets/logo.png" />
        <HelloWorld msg="Welcome to Your Vue.js App" />
      </div>
      <BottomNavbar />
    </section>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import BottomNavbar from "./components/BottomNavbar.vue";
export default {
  name: "app",
  components: {
    HelloWorld,
    BottomNavbar
  }
};
</script>

<style >
body {
  margin: 0;
  padding: 0;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.desktop-layout {
  display: grid;
  grid-template-columns: 250px 1fr;
  height: 100vh;
}

.left-navbar {
  background: #6cb2eb;
}

.tabs-container {
  list-style: none;
  font-weight: 500;
  color: #eff8ff;
  margin: 0;
  padding: 0;
}

.tab-option {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 70px;
  transition: 0.1s ease-in;
}
.tab-option:hover {
  cursor: pointer;
  background: #3490dc;
}
@media (max-width: 1024px) {
  .left-navbar {
    display: none;
  }
  .desktop-layout {
    grid-template-columns: 1fr;
  }
}
</style>
