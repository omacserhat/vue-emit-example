<template>
  <div>
  <div id="app">
  <alt-component @toplamasonucu="gelen($event)"/>
  Üst Componente Gelen Değer{{hesaplama}}
  </div>
  </div>
  </template>


  <script>
  import AltComponent from "./components/AltComponent.vue";
  export default {
  name: "App",
  data() {
  return {
  hesaplama: 0
  };
  },
  methods: {
  gelen(sonuc) {
  this.hesaplama = sonuc;
  }
  },
  components: {
  AltComponent
  }
  };
  </script>
  