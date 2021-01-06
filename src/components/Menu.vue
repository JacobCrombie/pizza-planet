<template>
  <div class="menu-wrapper">
    <!-- menu -->
    <div class="menu">
      <h3>~ Authentic handmade pizza~</h3>
      <table>
        <tbody>
          <tr>
            <td>
              <strong>~Pepperoni~</strong>
            </td>
          </tr>
          <tr>
            <td>
              <small
                >Lorem ipsum dolor sit amet consectetur adipisicing elit.
                Consequatur optio exercitationem esse dolores non, minus ratione
                hic ducimus libero itaque! Hic fugit consequatur, repellendus
                saepe natus expedita nulla soluta quia.</small
              >
            </td>
          </tr>
          <tr>
            <td>9"</td>
            <td>$6.95</td>
            <td>
              <button type="button" class="btn-green">+</button>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>



<style scoped>
h3 {
  text-align: center;
}
.menu-wrapper {
  display: flex;
  flex-direction: column;
}
.menu {
  background: #f1e6da;
  border-radius: 3px;
  height: 100vh;
  margin: 10px;
  padding: 10px;
}
@media screen and (min-width: 900px) {
  .menu-wrapper {
    flex-direction: row;
    justify-content: space-between;
  }
  .menu {
    width: 65vw;
  }
}
</style>