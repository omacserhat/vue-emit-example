<template>
    <div>
    <p>Alt Component</p>
    <p>Sayı 1</p>
    <input type="text" v-model="sayi1">
    <p>Sayı 2</p>
    <input type="text" v-model="sayi2">
    <button @click="topla()">Üst'e Gönder</button>
    </div>
    </template>
    <script>
    export default {
    name: "AltComponent",
    data() {
    return {
    sayi1: 0,
    sayi2: 0,
    };
    },
    methods: {
    topla() {
    let sonuc = +this.sayi1 + +this.sayi2;
    this.$emit("toplamasonucu", sonuc);
    }
    }
    };
    </script>