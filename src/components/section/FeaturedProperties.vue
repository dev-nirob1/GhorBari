<script setup>
import PropertiesCard from '../Widget/PropertiesCard.vue';

const properties = [
  {
    title: "Luxury Villa in Dhanmondi",
    location: "Dhanmondi, Dhaka",
    bedrooms: 4,
    bathrooms: 3,
    area: 2500,
    image: "https://images.unsplash.com/photo-1600585154340-be6161a56a0c?auto=format&fit=crop&w=1650&q=80"
  },
  {
    title: "Modern Apartment in Banani",
    location: "Banani, Dhaka",
    bedrooms: 3,
    bathrooms: 2,
    area: 1800,
    image: "https://images.unsplash.com/photo-1600585154340-be6161a56a0c?auto=format&fit=crop&w=1650&q=80"
  },
  {
    title: "Family House in Uttara",
    location: "Uttara, Dhaka",
    bedrooms: 4,
    bathrooms: 3,
    area: 2200,
    image: "https://images.unsplash.com/photo-1600585154340-be6161a56a0c?auto=format&fit=crop&w=1650&q=80"
  }
]
</script>
<template>
  <section class="featured-properties">
    <div class="container">
      <BaseTitle class="mb-2 text-center">Featured Properties</BaseTitle>
      <div class="medium-2 large-3 gap-2">
        <PropertiesCard v-for="(data, i) in properties" :key="i" :data="data"></PropertiesCard>
      </div>
    </div>
  </section>
</template>

<style>
.featured-properties {
  padding: 3.75rem 0;
}
</style>
