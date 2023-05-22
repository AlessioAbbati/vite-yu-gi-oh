<script>
import AppHeader from "./components/AppHeader.vue";
import CardsList from './components/CardsList.vue';
import axios from 'axios';
import { store } from './store';
import AppResults from './components/AppResults.vue';


export default {
  data() {
    return {
      store,
    }
  },
  components: { 
    AppHeader,
    CardsList,
    AppResults,
     
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
    <app-results />
    <cards-list />
  </main>
</template>

<style lang="scss">
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
main {
  padding-top: 8rem;
  padding-bottom: 8rem;
  background-color: #D48F38;
  display: grid;
  place-items: center;
}
</style>
