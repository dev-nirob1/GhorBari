<script setup>
import PropertiesCard from '../Widget/PropertiesCard.vue';

const properties = [
  {
    "title": "Luxury Villa in Dhanmondi",
    "location": "Dhanmondi, Dhaka",
    "bedrooms": 4,
    "bathrooms": 3,
    "area": 2500,
    "image": "https://cdn.pixabay.com/photo/2021/09/13/06/26/apartment-6620407_1280.jpg"
  },
  {
    "title": "Modern Apartment in Banani",
    "location": "Banani, Dhaka",
    "bedrooms": 3,
    "bathrooms": 2,
    "area": 1800,
    "image": "https://cdn.pixabay.com/photo/2023/12/30/07/31/living-room-8477525_1280.jpg"
  },
  {
    "title": "Family House in Uttara",
    "location": "Uttara, Dhaka",
    "bedrooms": 4,
    "bathrooms": 3,
    "area": 2200,
    "image": "https://cdn.pixabay.com/photo/2023/12/11/06/21/kitchen-8442907_640.jpg"
  },
  {
    "title": "Elegant Duplex in Gulshan",
    "location": "Gulshan, Dhaka",
    "bedrooms": 5,
    "bathrooms": 4,
    "area": 3000,
    "image": "https://images.pexels.com/photos/18567185/pexels-photo-18567185.jpeg?_gl=1*9kp4bv*_ga*OTAzOTgwMTguMTczNzAwNTI1OA..*_ga_8JE65Q40S6*czE3NTI1ODYxNDUkbzIyJGcxJHQxNzUyNTg2MjAxJGo0JGwwJGgw"
  },
  {
    "title": "Cozy Flat in Mirpur",
    "location": "Mirpur, Dhaka",
    "bedrooms": 2,
    "bathrooms": 2,
    "area": 1200,
    "image": "https://cdn.pixabay.com/photo/2016/11/22/23/38/apartment-1851201_1280.jpg"
  },
  {
    "title": "Spacious House in Baridhara",
    "location": "Baridhara, Dhaka",
    "bedrooms": 4,
    "bathrooms": 3,
    "area": 2600,
    "image": "https://cdn.pixabay.com/photo/2024/09/17/11/19/real-estate-9053405_960_720.jpg"
  }
]

</script>
<template>
      <!-- ======== Featured Properties section ======== -->
  <section id="properties" class="featured-properties bg-light">
    <div class="container">
      <BaseTitle class="mb-2 text-center">Featured Properties</BaseTitle>
      <div class="medium-2 large-3 gap-2">
        <!-- ===== individual property card =======  -->
        <PropertiesCard v-for="(data, i) in properties" :key="i" :data="data"/>
      </div>
    </div>
  </section>
</template>

<style>
.featured-properties {
  padding: 3.75rem 0;
}
</style>
