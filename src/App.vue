<template>
  <div id="app">
    <ProductDetails />
  </div>
</template>

<script>
import ProductDetails from './components/ProductDetails.vue';

export default {
  name: 'App',
  components: {
    ProductDetails
  },

  data() {
    return {
      isAuthenticated: false,
      users: [
        { id: 1, firstName: 'Иван', lastName: 'Иванов', email: 'ivan@example.com' },
        { id: 2, firstName: 'Петр', lastName: 'Петров', email: 'petr@example.com' },
        { id: 3, firstName: 'Анна', lastName: 'Сидорова', email: 'anna@example.com' }
      ],
    };
  },

}
</script>

<style></style>
