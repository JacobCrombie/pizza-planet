<template>
  <div class="menu-wrapper">
    <!-- menu -->
    <div class="menu">
      <h3>~ Authentic handmade pizza~</h3>
      <table v-for="item in getMenuItems" :key="item.name">
        <tbody>
          <tr>
            <td>
              <strong>~{{ item.name }}~</strong>
            </td>
          </tr>
          <tr>
            <td>
              <small>{{ item.description }}</small>
            </td>
          </tr>
          <tr v-for="(option, index) in item.options" :key="option[index]">
            <td>{{ option.size }}"</td>
            <td>${{ option.price }}</td>
            <td>
              <button
                type="button"
                class="btn-green"
                @click="addToBasket(item, option)"
              >
                +
              </button>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
    <!-- basket -->
    <div class="basket">
      <h3>~Basket~</h3>
      <table>
        <tbody>
          <tr>
            <td>
              <button class="btn-green">&#8722;</button>
              <span>2</span>
              <button class="btn-green">&#43;</button>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      basket: [],
      getMenuItems: {
        1: {
          name: "Margherita",
          description: "A delicious tomato based pizza topped with mozzarella",
          options: [
            {
              size: 9,
              price: 6.95,
            },
            {
              size: 12,
              price: 10.95,
            },
          ],
        },
        2: {
          name: "Pepperoni",
          description:
            "A delicious tomato based pizza topped with mozzarella and pepperoni",
          options: [
            {
              size: 9,
              price: 7.95,
            },
            {
              size: 12,
              price: 12.95,
            },
          ],
        },
        3: {
          name: "Ham and Pineapple",
          description:
            "A delicious tomato based pizza topped with mozzarella, ham and pineapple",
          options: [
            {
              size: 9,
              price: 7.95,
            },
            {
              size: 12,
              price: 12.95,
            },
          ],
        },
      },
    };
  },
  methods: {
    async addToBasket(item, option) {
      let pizzaExists = await this.basket.find(
        (pizza) => pizza.name === item.name && pizza.size === option.size
      );
      if (pizzaExists) {
        pizzaExists.quantity++;
        return;
      }
      this.basket.push({
        name: item.name,
        price: item.price,
        size: option.size,
        quantity: 1,
      });
    },
  },
};
</script>



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