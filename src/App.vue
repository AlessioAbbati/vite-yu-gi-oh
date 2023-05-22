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
  <cards-list />
</template>

<style lang="scss">

</style>
