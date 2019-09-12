<template>
  <div id="layout">
    <Sidebar/>
    <Header/>

    <main>
      <Nuxt/>
    </main>
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import Sidebar from "@/components/Sidebar.vue";

export default {
  components: {
    Header,
    Sidebar
  }
};
</script>


<style lang="scss">
@import "~assets/vars.scss";
@import url("https://fonts.googleapis.com/css?family=Lexend+Deca:100,300,400,600,700,800,900&display=swap");
@import url("https://fonts.googleapis.com/css?family=Russo+One&display=swap");

@keyframes pulse {
  0% {
    -moz-box-shadow: 0 0 0 0 var(--accent);
    box-shadow: 0 0 0 0 var(--accent);
  }
  70% {
    -moz-box-shadow: 0 0 0 2px var(--accent);
    box-shadow: 0 0 0 2px var(--accent);
  }
  100% {
    -moz-box-shadow: 0 0 0 0 var(--accent);
    box-shadow: 0 0 0 0 var(--accent);
  }
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  outline: var(--accent);
  font-family: Lexend Deca, sans-serif;
}

ul {
  list-style: none;
}

button {
  cursor: pointer;
}

#layout {
  background-color: var(--background);
  color: var(--foreground);
  font-family: Lexend Deca, sans-serif;
  display: grid;
  grid-template-columns: 1fr 5fr 2fr;
  grid-template-rows: 70px calc(100vh - 70px);
  grid-template-areas:
    "header header header"
    "menu main sidebar";
  header {
    grid-area: header;
  }
  aside {
    grid-area: menu;
  }
  main {
    grid-area: main;
  }
  section#action-bar {
    grid-area: sidebar;
  }
}
</style>
