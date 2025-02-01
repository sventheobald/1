<template>
    <div>
      <h1>Über Uns</h1>
      <p>Dies ist die About-Seite.</p>
      <button @click="goHome">Zurück zur Startseite</button>
    </div>
  </template>
  
  <script>
  export default {
    methods: {
      goHome() {
        this.$router.push('/');  // Navigiert zurück zur Startseite
      }
    }
  };
  </script>