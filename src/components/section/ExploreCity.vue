<template>
  <section class="explore-cities">
    <div class="container">
      <h3 class="section-title">Explore Properties by City</h3>
      <p class="section-subtitle">
        Find homes, apartments, and spaces in your favorite cities.
      </p>

      <div class="city-grid">
        <div class="city-card" v-for="(city, index) in cities" :key="index">
          <img :src="city.image" :alt="city.name" />
          <div class="city-name">{{ city.name }}</div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const cities = [
  {
    name: "Dhaka",
    image: "https://images.unsplash.com/photo-1630987871777-f7b2d62894d0?q=80&w=870&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
  },
  {
    name: "Chittagong",
    image: "https://images.unsplash.com/photo-1670550689583-1f71472a6405?q=80&w=774&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
  },
  {
    name: "Sylhet",
    image: "https://images.unsplash.com/photo-1690617629187-2fe116d5089f?q=80&w=774&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
  },
  {
    name: "Rajshahi",
    image: "https://images.unsplash.com/photo-1666554363523-69b5ce8b54d0?q=80&w=1032&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
  },
  {
    name: "Khulna",
    image: "https://images.pexels.com/photos/2382896/pexels-photo-2382896.jpeg?_gl=1*b13762*_ga*OTAzOTgwMTguMTczNzAwNTI1OA..*_ga_8JE65Q40S6*czE3NTI1OTEyNjUkbzIzJGcxJHQxNzUyNTkxMzQyJGo1OCRsMCRoMA..",
  },
  {
    name: "Barisal",
    image: "https://images.unsplash.com/photo-1561191223-2b9c2ee42b23?q=80&w=774&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
  },
];
</script>
<style scoped>
.explore-cities {
  padding: 4rem 1rem;
  background-color: #f3f4f6;
  text-align: center;
}

.explore-cities .section-title {
  font-size: 2rem;
  font-weight: bold;
  color: #1f2937;
  margin-bottom: 0.5rem;
}

.explore-cities .section-subtitle {
  color: #6b7280;
  font-size: 1rem;
  margin-bottom: 2rem;
}

.city-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.5rem;
}

.city-card {
  position: relative;
  overflow: hidden;
  border-radius: 10px;
  cursor: pointer;
  transition: transform 0.3s ease;
}

.city-card img {
  width: 100%;
  height: 220px;
  object-fit: cover;
  display: block;
  transition: transform 0.4s ease;
}

.city-card:hover img {
  transform: scale(1.05);
}

.city-name {
  position: absolute;
  bottom: 0;
  width: 100%;
  background: rgba(0, 0, 0, 0.45);
  color: white;
  padding: 0.75rem;
  font-size: 1.1rem;
  font-weight: 600;
  text-align: center;
}
</style>
