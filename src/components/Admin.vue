<template>
  <div class="admin-wrapper">
    <div class="current-user-wrapper"></div>
    <div class="menu-wrapper">
      <h3>Menu:</h3>
      <table>
        <thead>
          <tr>
            <th>Item</th>
            <th>Remove from menu</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>Margherita</td>
            <td>
              <button type="button" class="btn-red">&times;</button>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="orders-wrapper">
      <h3>Current Orders (5)</h3>
      <table>
        <thead>
          <tr>
            <th>Item</th>
            <th>Size</th>
            <th>Quantity</th>
            <th>Price</th>
          </tr>
        </thead>
        <tbody>
          <tr class="order-number">
            <th colspan="4">
              <strong>Order Number: 4</strong>
              <button type="button" class="btn-red">&times;</button>
            </th>
          </tr>
          <tr>
            <td>Margherita</td>
            <td>9"</td>
            <td>2</td>
            <td>$13</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>


<script>
export default {
  name: "admin",
  data() {
    return {};
  },
  computed: {},
  methods: {},
  components: {},
};
</script>


<style scoped>
.admin-wrapper {
  margin: 10px;
}
.current-user-wrapper,
.order-wrapper,
.menu-wrapper {
  margin: 10px 0;
  padding: 10px;
  border: solid 1px #f79e38;
}
table {
  text-align: left;
  width: 70vw;
}
.order-number th {
  background: #ddd;
}
.order-number button {
  margin: 0 10px;
}
</style>