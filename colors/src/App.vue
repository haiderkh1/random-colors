<template>
  <div id="app">
    <Header v-bind:color="color" />
    <BtnChangeBack v-bind:color="color" v-on:cambiar-fondo="cambioElFondo" />
    <Footer />
  </div>
</template>

<script>
import BtnChangeBack from "./components/BtnChangeBack.vue";
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
export default {
  name: "App",
  components: {
    BtnChangeBack,
    Header,
    Footer,
  },
  data() {
    return {
      color: "",
    };
  },

  created: function() {
    this.changeColor();
    document.addEventListener("keydown", (e) => {
      if (e.code === "Space") this.changeColor();
    });
  },

  watch: {
    color: function(val) {
      document.body.style.backgroundColor = val;
    },
  },

  methods: {
    changeColor: function() {
      this.color = "#" + Math.floor(Math.random() * 6777215).toString(16);
    },
    cambioElFondo: function() {
      this.color = "newColor";
    },
  },
};
</script>

<style>
*,
*::after,
*::before {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
body {
  transition: all 300ms;
  font-family: system-ui, sans-serif;
}
</style>
