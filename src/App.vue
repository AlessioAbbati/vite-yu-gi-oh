<script>
import AppHeader from "./components/AppHeader.vue";
import CardsList from './components/CardsList.vue';
import axios from 'axios';
import { store } from './store';


export default {
  data() {
    return {
      store,
    }
  },
  components: { 
    AppHeader,
    CardsList,
     
  },
};


</script>

<template>
  <app-header />
  <main>
    <cards-list />
  </main>
</template>

<style lang="scss">
main {
  background-color: #D48F38;
  height: 100vh;
}
</style>
