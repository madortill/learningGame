<template>
  <div id="app">
    <header v-if="showHeader" class="logo-bar">
      <div class="logo-group">
        <img src="/src/assets/media/kiryathadracha.svg" alt="mifkada-logo" class="logo" />
        <img src="/src/assets/media/hadraha.png" alt="hadraha-logo" class="logo" />
      </div>
    </header>

    <main v-if="showLoader" class="main-content">
      <Loader />
    </main>
    <div v-if="showHeader">
      <HomePage></HomePage>
      <Buttons></Buttons>
    </div>
    <AboutPage v-if="showHeader" />
  </div>
</template>


<script>
import Loader from "@/components/Loader.vue";
import AboutPage from "@/components/About.vue";
import HomePage from "@/components/HomePage.vue";
import Buttons from "@/components/Buttons.vue";

export default {
  name: "app",
  components: {
    Loader,
    AboutPage,
    HomePage,
    Buttons
  },
  data() {
    return {
      showLoader: true,
      showHeader: false,
    };
  },
  mounted() {
    setTimeout(() => {
      this.showLoader = false;
      this.showHeader = true;
    }, 4000);
  },
};
</script>

<style>
@font-face {
  font-family: "Assistant";
  src: url("@/assets/fonts/Assistant-VariableFont_wght.ttf");
}



* {
  font-family: "Assistant";
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  direction: rtl;
}

html,
body {
  height: 100%;
  overflow-x: hidden !important;
  overflow-y: auto;
}

#app {
  min-height: 100vh;
  min-width: 100vw;
  max-width: 100vw;
  overflow-x: hidden;
  background-color: #90e0ef;
  display: flex;
  flex-direction: column;
  width: 100vw;
}


.logo-bar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem;
  flex-wrap: wrap;
  background-color: rgba(255, 255, 255, 0.2);
}

.logo-group {
  display: flex;
  gap: 1rem;
  align-items: center;
}

.logo {
  height:4.8rem;
  width: auto;
  max-width: 100%;
}

.main-content {
  flex-grow: 1;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 2rem;
}
</style>
