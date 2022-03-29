<template>
  <div>
    <section id="head" class="my-container">
      <div class="image-dc">
        <img src="../assets/img/dc-logo.png" alt="DC logo" />
      </div>
      <div>
        <ul>
          <li
            v-for="(element, index) in listContent"
            :class="{ active: element.current }"
            :key="index"
          >
            <a :class="{ active: element.current }" href="">{{
              element.text
            }}</a>
          </li>
        </ul>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "IndexHeader",
  data: function () {
    return {
      listContent: [
        {
          text: "character",
          current: false,
        },
        {
          text: "Comics",
          current: true,
        },
        {
          text: "Movies",
          current: false,
        },
        {
          text: "tv",
          current: false,
        },
        {
          text: "games",
          current: false,
        },
        {
          text: "collectibles",
          current: false,
        },
        {
          text: "videos",
          current: false,
        },
        {
          text: "fans",
          current: false,
        },
        {
          text: "news",
          current: false,
        },
        {
          text: "shop",
          current: false,
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/style.scss";
@import "../assets/scss/partial/_variables.scss";
section#head,
div,
ul,
li {
  display: flex;
}
section#head,
div {
  align-items: center;
}

section#head {
  height: 100px;
  justify-content: space-between;

  div {
    height: 100%;
    margin-left: 1rem;

    img {
      width: 80%;
      min-width: 80px;
    }
  }
  ul {
    height: 100%;
    margin-right: 1rem;
    align-content: center;
    li {
      list-style-type: none;
      margin: 0 0.5rem;
      border-bottom: 2px solid transparent;
      line-height: 100px;

      &:hover,
      &.active {
        border-bottom: 2px solid $brandColor;
      }
      a {
        text-decoration: none;
        text-transform: uppercase;
        color: black;
        &:hover,
        &.active {
          color: $brandColor;
        }
      }
    }
  }
}
</style>
