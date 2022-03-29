<template>
  <div class="bg-primary">
    <section id="Icons-dc" class="my-container">
      <div v-for="(element, index) in listIcons" :key="index" class="mini-card">
        <img
          :src="require(`../assets/img/${element.image}`)"
          :alt="element.text"
        />
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
          image: "buy-comics-digital-comics.png",
        },
        {
          text: "dc merchandise",
          image: "buy-comics-merchandise.png",
        },
        {
          text: "subscription",
          image: "buy-comics-subscriptions.png",
        },
        {
          text: "comic shop locator",
          image: "buy-comics-shop-locator.png",
        },
        {
          text: "dc power visa",
          image: "buy-dc-power-visa.svg",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/style.scss";
@import "../assets/scss/partial/_variables.scss";

.bg-primary {
  background-color: $brandColor;
}
#Icons-dc {
  height: 100px;
  justify-content: space-evenly;
  div {
    height: 50%;
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

#Icons-dc,
.mini-card {
  display: flex;
  align-items: center;
}
</style>