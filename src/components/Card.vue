<script>
export default {
    props: {
        CardData: Object,
    },
};
</script>

<template>
  <div>
    <img :src="CardData.card_images" :alt="CardData.name">
    <h3>{{ CardData.name }}</h3>
    <div class="archetype">{{ CardData.archetype }}</div>

  </div>
</template>

<style lang="scss" scoped>

</style>