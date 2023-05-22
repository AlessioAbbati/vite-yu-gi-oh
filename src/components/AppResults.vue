<script>
import {store} from '../store';
export default {
    data() {
        return {
            store,
        }
    }
}

</script>

<template>
  <div class="results">
    <span>Found {{ store.CardsList.length }} Cards</span> 
  </div>
</template>

<style lang="scss" scoped>
  .results {
    width: 90%;
    height: 3rem;
    background-color: #212529;
    color: white;
    display: flex;
    align-items: center;
    span {
        margin-left: 1rem;
    }
  }
</style>

