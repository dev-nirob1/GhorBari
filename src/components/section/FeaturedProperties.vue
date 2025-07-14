<!-- FeaturedProperties.vue -->
<template>
  <section class="featured">
    <div class="container">
      <h2 class="section-title">🏡 Featured Properties</h2>
      <div class="properties-grid">
        <div v-for="(property, index) in properties" :key="index" class="property-card">
          <img :src="property.image" :alt="property.title" />
          <div class="property-info">
              <p>{{ property.location }}</p>
              <h3>{{ property.title }}</h3>
            <ul class="features">
              <li>🛏️ {{ property.bedrooms }} Bed</li>
              <li>🛁 {{ property.bathrooms }} Bath</li>
              <li>📐 {{ property.area }} sqft</li>
            </ul>
            <button class="view-btn">View Details</button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const properties = [
  {
    title: "Luxury Villa in Dhanmondi",
    location: "Dhanmondi, Dhaka",
    price: "৳ 85,00,000",
    bedrooms: 4,
    bathrooms: 3,
    area: 2500,
    image: "https://images.unsplash.com/photo-1600585154340-be6161a56a0c?auto=format&fit=crop&w=1650&q=80"
  },
  {
    title: "Modern Apartment in Banani",
    location: "Banani, Dhaka",
    price: "৳ 62,00,000",
    bedrooms: 3,
    bathrooms: 2,
    area: 1800,
    image: "https://images.unsplash.com/photo-1600585154340-be6161a56a0c?auto=format&fit=crop&w=1650&q=80"
  },
  {
    title: "Family House in Uttara",
    location: "Uttara, Dhaka",
    price: "৳ 72,00,000",
    bedrooms: 4,
    bathrooms: 3,
    area: 2200,
    image: "https://images.unsplash.com/photo-1600585154340-be6161a56a0c?auto=format&fit=crop&w=1650&q=80"
  }
]
</script>

<style scoped>
.featured {
  background: #f9f9f9;
  padding: 4rem 1.5rem;
}

.container {
  max-width: 1200px;
  margin: auto;
}

.section-title {
  text-align: center;
  font-size: 2rem;
  color: var(--primary-color);
  margin-bottom: 2rem;
}

.properties-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
}

.property-card {
  background: white;
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.08);
  transition: transform 0.3s;
}

.property-card:hover {
  transform: translateY(-5px);
}

.property-card img {
  width: 100%;
  height: 250px;
  object-fit: cover;
}

.property-info {
  padding: 1rem;
}

.property-info h3 {
  color: var(--primary-color);
  font-size: 1.2rem;
}

.property-info p {
    margin: 0;
 margin-bottom: .75rem;
}

.features {
  list-style: none;
  display: flex;
  flex-wrap: wrap;
  gap: 0.8rem;
  padding: 0;
  margin: 0.5rem 0 1rem 0;
  font-size: 0.9rem;
  color: #555;
}

.view-btn {
  background: var(--primary-color);
  color: white;
  padding: 1rem 1.8rem;
  border: none;
  border-radius: 6px;
  font-weight: 600;
  cursor: pointer;
  transition: background 0.3s;
}

.view-btn:hover {
  background: var(--primary-light-color);
  color: var(--primary-color);
}
</style>
