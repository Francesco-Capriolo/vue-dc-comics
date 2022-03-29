<template>
  <div class="card-element">
    <img :src="herObject.thumb" :alt="herObject.type" />
    <h3>
      {{ herObject.series }}
    </h3>
  </div>
</template>

<script>
export default {
  name: "HeroCard",
  props: ["herObject"],
};
</script>

<style lang="scss" scoped>
.card-element {
  width: calc(100% / 7);
  margin: 0.5rem;
  img {
    width: 100%;
  }
  h3 {
    padding: 0.3rem;
    color: white;
  }
}
</style>