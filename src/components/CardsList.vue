<script>
import Card from "./Card.vue"
import { store } from '../store';

export default {
    data() {
        return {
            store,
        }
    },
    components: { 
        Card,
    },
}


</script>

<template>
  <div class="cards-list">
     <card 
        v-for="Card in store.CardsList"
        :key="Card.id"
        :CardData="Card"
     />
  </div>
</template>

<style lang="scss" scoped>
  .cards-list {
    background-color: white;
    display: flex;
    flex-wrap: wrap;
    width: 80%;
    padding: 3rem;
  }
</style>