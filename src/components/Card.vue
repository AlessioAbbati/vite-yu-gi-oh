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
    <h3>{{ CardData.name }}</h3>
    <div class="archetype">{{ CardData.archetype }}</div>

  </div>
</template>

<style lang="scss" scoped>

</style>