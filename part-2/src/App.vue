<script setup>
import { computed, ref } from "vue";

const products = ref([
  { id: 1, name: "Robot Programming eLearning Course", price: 24999, quantity: 0 },
  { id: 2, name: "Simulation Software License", price: 149910, quantity: 0 },
  { id: 3, name: "Cloud Monitoring Subscription (1 Year)", price: 79950, quantity: 0 }
]);

const total = computed(() => {
  return Math.round(
    products.value.reduce((acc, product) => acc + product.price * product.quantity, 0) / 100
  );
});

function increaseQuantity(product) {
  product.quantity += 1;
}

function decreaseQuantity(product) {
  product.quantity -= 1;
}
</script>

<template>
  <div class="flex items-center justify-center h-screen w-screen text-gray-900">
    <div class="max-w-3xl w-full border border-gray-200 shadow-2xl rounded-md">
      <h2 class="text-4xl bg-gray-200 p-8">KUKA Shopping Cart</h2>
      <ul class="p-8">
        <li
          v-for="product in products"
          :key="product.id"
          class="flex flex-col my-2 w-full bg-gray-100 odd:bg-gray-200 p-4"
        >
          <span class="flex items-center justify-between w-full space-x-3">
            <span class="w-1/3">{{ product.name }}</span>
            <span>{{ product.price / 100 }}€</span>
            <span class="inline-flex items-center justify-between space-x-3">
              <button
                class="bg-primary hover:bg-primary-600 py-1 px-2 rounded-md"
                @click="decreaseQuantity(product)"
              >
                -
              </button>
              <span class="w-12 text-center">{{ product.quantity }}</span>
              <button
                class="bg-primary hover:bg-primary-600 py-1 px-2 rounded-md"
                @click="increaseQuantity(product)"
              >
                +
              </button>
            </span>
            <span class="w-16 text-right">
              {{ (product.price * product.quantity) / 100 }}€
            </span>
          </span>
        </li>
      </ul>
      <p class="flex items-center justify-between text-3xl mt-4 p-8">
        <span>Total:</span>
        <span class="font-bold">{{ total }}€</span>
      </p>
    </div>
  </div>
</template>
