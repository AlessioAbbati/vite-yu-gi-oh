<script>
import AppHeader from "./components/AppHeader.vue";
import CardsList from './components/CardsList.vue';
import axios from 'axios';
import { store } from './store';
import AppResults from './components/AppResults.vue';
import ClassChoose from './components/ClassChoose.vue';


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
    ClassChoose,
     
  },
  methods: {
    requestDataFromApi() {
      axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php', )   
     .then(response => (this.store.ArrArchetypes = response.data));
    },
    filteredArchetypes() {
      axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php', {
        params: {
          archetype: this.store.searchArchetypes,
        }
      })
      .then(response => (this.store.CardsList = response.data.data));
    }
  }, 
  created() {
    axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=50&offset=0')
    .then(response => (this.store.CardsList = response.data.data));

    this.requestDataFromApi();
    
  }
};


</script>

<template>
  <app-header />
  <main>
    <class-choose @performSearch="filteredArchetypes"/>
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
