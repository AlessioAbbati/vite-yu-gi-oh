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
    found {{ store.CardsList.length }}
  </div>
</template>

<style lang="scss" scoped>
  .results {
    width: 80%;
    height: 3rem;
    background-color: #212529;
  }
</style>

