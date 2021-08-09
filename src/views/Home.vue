<template>
  <div class="home">
    <div class="content">
      <Navbar />
      <br>
      <h3 class="row gx-3 gy-2 align-items-center"><center>ลอตเตอรี่ออนไลน์</center></h3>
      <p class="row gx-3 gy-2 align-items-center text-danger"><center>ลอตเตอรี่งวดวันที่ {{ deadlinedate }}</center></p>
      <h3 class="row gx-3 gy-2 align-items-center">
        <center>Comming Soon: {{ deadlinedate }}</center>
      </h3>
      <flip-countdown :deadline="deadline1ts"></flip-countdown>
      <Lotto />
 <section class="products">
    <div v-for="product in products" :key="product.id" class="product">
      <h3 class="product__header">{{ product.name }}</h3>
      <img
        src="https://via.placeholder.com/150"
        :alt="product.name"
        class="product__image"
      >
      <p class="product__description">{{ product.description }}</p>
      <div class="cart">
        <button
          @click="updateCart(product, 'subtract')"
          class="cart__button"
        >
          -
        </button>
        <span class="cart__quantity">{{ product.quantity }}</span>
        <button
          @click="updateCart(product, 'add')"
          class="cart__button"
        >
          +
        </button>
      </div>
    </div>
  </section>  
    <h2 class="nav__header">Products</h2>
    <div class="nav__cart">
      <button @click="showCart = !showCart">
        <i class="fas fa-shopping-cart"></i>
      </button>
      <span class="total-quantity">{{ totalQuantity }}</span>
      <div v-if="showCart" class="cart-dropdown">
        <ul class="cart-dropdown__list">
          <li
            v-for="product in cart"
            :key="product.id"
          >
            {{ product.name }} ({{ product.quantity }})
          </li>
        </ul>
      </div>
    </div>
    </div>
    <Footer />
  </div>
</template>

<script>
import FlipCountdown from "vue2-flip-countdown";
import Navbar from "../components/Navbar.vue";
import Footer from "../components/Footer.vue";
import Lotto from "../components/Lotto.vue";

import moment from "moment";
//const fmt = "YYYY-MM-DD";
const DASH_DMY = 'DD-MM-YYYY';
export default {
  name: "app",
  components: {
    FlipCountdown,
    Navbar,
    Footer,
    Lotto,
  },
  data() {
    return {
      deadline1ts: "2021-10-01",
      deadlinedate :"01-10-2021",
      showCart: false,
     products: [
        {
          id: 1,
          name: 'Product 1',
          description: 'This is an incredibly awesome product',
          quantity: 0,
        },
        {
          id: 2,
          name: 'Product 2',
          description: 'This is an incredibly awesome product',
          quantity: 0,
        },
        {
          id: 3,
          name: 'Product 3',
          description: 'This is an incredibly awesome product',
          quantity: 0,
        }
      ],
    };
  },
  computed: {
    deadline1: function () {
      return moment(this.deadlinedate).format(DASH_DMY); 
    },
    cart() {
      return this.products.filter(product => product.quantity > 0);
    },
    totalQuantity() {
      return this.products.reduce(
        (total, product) => total + product.quantity,
        0
      );
    }
    },
  methods: {
    timeElapsedHandler: function () {},
          updateCart(product, updateType) {      
        for (let i = 0; i < this.products.length; i++) {
          if (this.products[i].id === product.id) {
            if (updateType === 'subtract') {
              if (this.products[i].quantity !== 0) {
                this.products[i].quantity--;
              }
            } else {
              this.products[i].quantity++;
            }
            
            break;
          }
        }
      }
  },
};
</script>
<style>
.products {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
.description {
      font-size: 1.3rem;
      margin-top: 1rem;
    }
.cart {
  margin-top: 2rem;
  text-align: center;
}
.button {
    background: lightblue;
    border: 0;
    color: white;
    cursor: pointer;
    font-size: 1.5rem;
    font-weight: bold;
    height: 2.5rem;
    width: 2.5rem;
  }
  .quantity {
    font-size: 1.5rem;
    margin: 0 1rem;
  }
    .image {
      display: block;
      margin: 1rem auto;
    }
  .product {
    border: 1px solid lightgray;
    border-radius: 10px;
    margin: 2rem;
    padding: 1rem; 
  }
</style>

