<script setup>
// import JSON from './components/JSON.vue'
import BHeader from './components/BHeader.vue';
// import Form from './views/HomeView.vue';
</script>

<template>
  <header>
    <BHeader />
  </header>

  <main>
    <!-- <JSON /> -->
     <!-- <Form /> -->
    <div class="container mt-5">
      <router-view />
    </div>
  </main>
</template>

<style >

  header {
    line-height: 1.5;
  }

  .container h1,p {
    text-align: center;
  }

  @media (min-width: 1024px) {
    header {
      display: flex;
      place-items: center;
      padding-right: calc(var(--section-gap) / 2);
    }

    .logo {
      margin: 0 2rem 0 0;
    }

  }

  .h1 {
    color: #df0000;
    font-size: 2.5rem;
  }

  .card {
  border: 1px solid #ccc;
  border-radius: 10px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }
  .card-header {
  background-color: #275FDA;
  color: white;
  padding: 10px;
  border-radius: 10px 10px 0 0;
  }
  .list-group-item {
  padding: 10px;
  }

  /* @media (min-width: 576px) {
    .card {
      width: 100%;
    }

  } */

  #buttons {
    display: flex;
    justify-content: space-between;
  }
</style>
