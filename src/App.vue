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
  created() {
    // richiesta API
    axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
       .then(response => (this.store.CardsList = response.data.data));
  }
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
  display: grid;
  place-items: center;
}
</style>
