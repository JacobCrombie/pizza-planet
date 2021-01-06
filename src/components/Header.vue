<template>
  <header class="appHeader">
    <div class="header-logo">
      <img src="../assets/images/planet.png" alt="pizza planet icon" />
      <h1 href="/">PIZZA PLANET</h1>
    </div>
    <nav>
      <ul>
        <li>
          <a href="/">Home</a>
        </li>
        <span>~</span>
        <li>
          <a href="/menu">Menu</a>
        </li>
        <span>~</span>
        <li>
          <a href="/contact">Contact Us</a>
        </li>
        <span>~</span>
        <li>
          <a href="/about">About Us</a>
        </li>
      </ul>
    </nav>
  </header>
</template>


<script>
export default {
  name: "appHeader",
  data() {
    return {};
  },
  computed: {},
  methods: {},
  components: {},
};
</script>


<style scoped>
h1 {
  font-size: 1.3em;
}
.header-logo {
  background-image: linear-gradient(
    45deg,
    #d85226 25%,
    #f79e38 25% 50%,
    #d85226 50% 75%,
    #f79e38 75%,
    #f79e38 100%
  );
  background-size: 80px 80px;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 10px;
}
.header-logo img {
  max-width: 25vw;
}
ul {
  padding: 10px 0;
}
li {
  display: inline-block;
}
@media screen and (min-width: 900px) {
  .header-logo img {
    max-width: 20vw;
  }
}
</style>