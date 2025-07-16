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
<template>
      <!-- ======== Explore cities section ======== -->
  <section id="cities" class="explore-cities bg-light">
    <div class="container">
      <BaseTitle class="text-center mb-2">Find Properties Across Top Cities</BaseTitle>

      <div class="medium-2 large-3 gap-2">
              <!-- ======== Explore cities card ======== -->
        <div class="city-card" v-for="(city, index) in cities" :key="index">
          <BaseImage :image="city.image" :alt="city.name" />
          <div class="city-name">{{ city.name }}</div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.explore-cities {
  padding: 3.75rem 0;
}

.city-card {
  position: relative;
  overflow: hidden;
  border-radius: 2rem 0;
  cursor: pointer;
  transition: all 0.5s ease;
}

.city-name {
  position: absolute;
  bottom: 0;
  width: 100%;
  background: rgb(from var(--secondary-color) r g b / 40%);
  color: var(--white-color);
  padding: 0.75rem;
  font-weight: 600;
  text-align: center;
}

.city-card img {
  width: 100%;
  height: 220px;
  object-fit: cover;
  display: block;
  transition: all 0.5s ease;
}

.city-card:hover img {
  transform: scale(1.1);
}
</style>
