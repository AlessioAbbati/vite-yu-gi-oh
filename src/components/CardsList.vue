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
        class="card-container"
     />
  </div>
</template>

<style lang="scss" scoped>
  .cards-list {
    background-color: white;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    width: 90%;
    padding: 3rem;
    
    .card-container {
      background-color: #D48F38;
      margin-inline: 1rem;
      margin-bottom: .6rem;
    }
  }
</style>