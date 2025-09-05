<script setup>
// import JSON from './components/JSON.vue'
import BHeader from './components/BHeader.vue';
import Form from './components/Form.vue';
</script>

<template>
  <header>
    <BHeader />
  </header>

  <main>
    <!-- <JSON /> -->
     <Form />
  </main>
</template>

<style scoped>
/* header {
  line-height: 1.5;
} */

/* @media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

} */
</style>
