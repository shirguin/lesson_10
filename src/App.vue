<template>
  <div id="app">
    <AuthenticationComp :isAuthenticated="isAuthenticated" />
    <UserList :users="users"/>
    <MortgageCalculator />
  </div>
</template>

<script>
import AuthenticationComp from './components/Authentication.vue';
import UserList from './components/UserList.vue';
import MortgageCalculator from './components/MortgageCalculator.vue';

export default {
  name: 'App',
  components: {
    AuthenticationComp,
    UserList,
    MortgageCalculator,
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
