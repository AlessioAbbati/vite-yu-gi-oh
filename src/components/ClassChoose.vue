<script>
import { store } from '../store';

export default {
    data() {
        return {
            store,
        }
    },
    methods: {
        emitArchetypes() {
            this.$emit('performSearch');
        },
        resetArchetypes() {
            this.$emit('resetSearch');
        }
    },
};
</script>

<template>
    <div class="search">
      <select v-model="store.searchArchetypes" @change="emitArchetypes">
      <option value="">Select Archetypes</option>
      <option v-for="archetype in store.ArrArchetypes" :key="archetype" :value="archetype.archetype_name">{{ archetype.archetype_name }}</option>
    </select>
    <button @click="resetArchetypes">Reset</button>
    </div>
</template>

<style lang="scss" scoped>
.search {
    padding-bottom: 5rem;
    select{
        padding: 1rem;
        &:hover {
            -webkit-box-shadow: 0px 0px 22px 16px rgba(219,178,96,1);
            -moz-box-shadow: 0px 0px 22px 16px rgba(219,178,96,1);
            box-shadow: 0px 0px 22px 16px rgba(219,178,96,1);
    }   }
}
button {
    padding: 1rem;
    margin-left: 1rem;
    &:hover {
        -webkit-box-shadow: 0px 0px 22px 16px rgba(219,178,96,1);
        -moz-box-shadow: 0px 0px 22px 16px rgba(219,178,96,1);
        box-shadow: 0px 0px 22px 16px rgba(219,178,96,1);
    }
}

</style>