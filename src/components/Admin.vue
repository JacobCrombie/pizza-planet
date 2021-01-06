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
    <div class="order-wrapper"></div>
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
</style>