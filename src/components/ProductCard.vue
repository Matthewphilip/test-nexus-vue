<template>
  <section class="product-card">
    <section class="product-image-container">
      <img
        class="product-image"
        src="../assets/Matthew2.jpg"
        alt="Product Image"
      />
      <img
        class="product-image"
        src="../assets/Matthew2.jpg"
        alt="Product Image"
      />
      <img
        class="product-image"
        src="../assets/Matthew2.jpg"
        alt="Product Image"
      />
      <p class="advert-tab">
        {{ formatTransmission(product.advert_classification) }}
      </p>
      <div class="spec-tab-container">
        <p class="spec-tab">{{ formattedOdometer }}</p>
        <p class="spec-tab">{{ product.fuel_type }}</p>
        <p class="spec-tab">{{ formatTransmission(product.transmission) }}</p>
        <p class="spec-tab">{{ product.body_type }}</p>
      </div>
    </section>
    <section class="product-model">
      <div class="spec">
        <h2>{{ product.plate }} {{ product.make }} {{ product.model }}</h2>
        <div class="advert-container">
          <div class="advert">
            {{ formatTransmission(product.advert_classification) }}
          </div>
          <i
            class="fas fa-star fa-lg icon-favorite"
            v-if="isFavorited"
            @click="toggleFavorite"
          ></i>
          <i
            class="fa-regular fa-star fa-lg"
            v-else
            @click="toggleFavorite"
          ></i>
        </div>
      </div>
      <p>{{ product.derivative }}</p>
    </section>
    <section class="product-details">
      <section class="mechanical">
        <p>{{ formattedOdometer }} | {{ product.fuel_type }}</p>
        <p>
          {{ formatTransmission(product.transmission) }} |
          {{ product.body_type }}
        </p>
      </section>
      <section class="finance">
        <p>
          <span class="monthly-price">£{{ monthlyPrice }}</span> /mo (PCP)
        </p>
        <p>£{{ product.price }} <span class="calculate">Calculate</span></p>
      </section>
    </section>
  </section>
</template>

<script>
export default {
  props: {
    product: Object,
  },

  data() {
    return {
      isFavorited: false,
    };
  },

  computed: {
    monthlyPrice() {
      return (this.product.price / 12).toFixed(2);
    },

    formattedOdometer() {
      if (typeof this.product.odometer_value === "number") {
        if (this.product.odometer_value.toString().length > 3) {
          return (this.product.odometer_value / 1000).toFixed(1) + "k miles";
        } else {
          return this.product.odometer_value + " miles";
        }
      } else {
        return this.product.odometer_value;
      }
    },
  },

  methods: {
    formatTransmission(transmission) {
      if (typeof transmission === "string") {
        return (
          transmission.charAt(0).toUpperCase() +
          transmission.slice(1).toLowerCase()
        );
      } else {
        return "";
      }
    },

    toggleFavorite() {
      this.isFavorited = !this.isFavorited;
    },
  },
};
</script>