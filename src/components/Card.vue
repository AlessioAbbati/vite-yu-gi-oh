<script>
export default {
    props: {
        CardData: Object,
    },
};
</script>

<template>
  <div>
    <img :src="CardData.card_images[0].image_url_small" :alt="CardData.id">
    <div class="text-container">
        <h3>{{ CardData.name }}</h3>
        <div class="archetype">{{ CardData.archetype }}</div>
    </div>

  </div>
</template>

<style lang="scss" scoped>
  .text-container {
    width: 168px;
    display: flex;
    flex-direction: column;
    align-items: center;
    h3 {
        color: white;
        text-align: center;
        padding-top: .5rem;
    }
    .archetype {
        padding-top: .5rem;
    }
  }
</style>