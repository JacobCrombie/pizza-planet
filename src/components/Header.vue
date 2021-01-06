<template>
  <header class="appHeader">
    <div class="header-logo">
      <img src="../assets/images/planet.jpg" alt="pizza planet icon" />
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
</style>