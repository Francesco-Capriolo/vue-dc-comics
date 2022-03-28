<template>
  <div>
    <section id="Icons-dc">
      <div v-for="(element, index) in listIcons" :key="index">
        <img :src="element.image" :alt="element.text" />
        <span>{{ element.text }}</span>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "IndexIconsDC",
  data: function () {
    return {
      listIcons: [
        {
          text: "digital comics",
          image: "../assets/img/buy-comics-digital-comics.png",
        },
        {
          text: "dc merchandise",
          image: "../assets/img/buy-comics-merchandise.png",
        },
        {
          text: "subscription",
          image: "../assets/img/buy-comics-subscriptions.png",
        },
        {
          text: "comic shop locator",
          image: "../assets/img/buy-comics-shop-locator.png",
        },
        {
          text: "dc power visa",
          image: "../assets/img/buy-dc-power-visa.svg",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/partial/_variables.scss";

#Icons-dc {
  height: 100px;
  background-color: $brandColor;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  div {
    height: 50%;
    display: flex;
    align-items: center;
  }
  img {
    height: 100%;
  }
  span {
    color: white;
    padding: 1rem;
    text-transform: uppercase;
  }
}
</style>