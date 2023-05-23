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
    },
};
</script>

<template>
    <select v-model="store.ArrArchetypes" @change="emitArchetypes">
      <option value="">Select Archetypes</option>
      <option v-for="archetype in store.ArrArchetypes" :key="archetype" :value="archetype">{{ archetype }}</option>
    </select>
</template>

<style lang="scss" scoped>

</style>