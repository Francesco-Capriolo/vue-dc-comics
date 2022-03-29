<template>
  <div>
    <div id="dc-footer">
      <div class="footer-list my-container">
        <div class="list list-comics">
          <ul>
            <h4>dc comics</h4>
            <li v-for="(element, index) in listContent" :key="index">
              {{ element.text }}
            </li>
          </ul>
          <ul class="list-shop">
            <h4>shop</h4>
            <li>Shop DC</li>
            <li>Shop DC Collectibles</li>
          </ul>
        </div>
        <div class="list">
          <ul>
            <h4>DC</h4>
            <li>Term Of Use</li>
            <li>Privacy policy</li>
            <li>Term Of Use</li>
            <li>Privacy policy</li>
            <li>Term Of Use</li>
            <li>Privacy policy</li>
            <li>Term Of Use</li>
            <li>Privacy policy</li>
            <li>Term Of Use</li>
            <li>Privacy policy</li>
            <li>Term Of Use</li>
          </ul>
        </div>
        <div class="list">
          <ul>
            <h4>sites</h4>
            <li>Term Of Use</li>
            <li>Privacy policy</li>
            <li>Term Of Use</li>
            <li>Privacy policy</li>
            <li>Term Of Use</li>
          </ul>
        </div>
      </div>
    </div>
    <section class="bg-dark">
      <div id="footer-bottom" class="my-container">
        <button class="button-signUp">sign-Up now!</button>
        <div class="follow">
          <h3>follow us</h3>
          <img src="../assets/img/footer-facebook.png" alt="" />
          <img src="../assets/img/footer-twitter.png" alt="" />
          <img src="../assets/img/footer-youtube.png" alt="" />
          <img src="../assets/img/footer-pinterest.png" alt="" />
          <img src="../assets/img/footer-periscope.png" alt="" />
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "IndexFooter",
  data: function () {
    return {
      listContent: [
        {
          text: "character",
          current: false,
        },
        {
          text: "Comics",
          current: false,
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

#dc-footer {
  height: 400px;
  background-image: url(../assets/img/footer-bg.jpg);
  background-position: center top;
  background-repeat: no-repeat;
  background-size: cover;
  .footer-list {
    display: flex;
    justify-content: flex-start;
    background-image: url(../assets/img/dc-logo-bg.png);
    background-size: no-repeat;
    background-position: right center;
    background-repeat: no-repeat;
    ul {
      padding: 1rem 1rem;
      li {
        color: gray;
        list-style-type: none;
        padding: 0.2rem 0;
      }
      h4 {
        color: white;
        padding: 0.5rem 0;
        text-transform: uppercase;
      }
    }
    .list-shop {
      padding-bottom: 3rem;
    }
  }
}
.bg-dark {
  background-color: #303030;
}
#footer-bottom {
  height: 100px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  button {
    color: white;
    text-transform: uppercase;
    background-color: #303030;
    border: 1px solid $brandColor;
    padding: 1rem;
    margin-left: 1rem;
  }
  .follow {
    display: flex;
    h3 {
      color: $brandColor;
      padding-top: 1rem;
      padding-right: 1rem;
      text-transform: uppercase;
    }
    img {
      padding: 0.5rem;
    }
  }
}
</style>
