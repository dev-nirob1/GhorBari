<!-- StatisticsSection.vue -->
<template>
  <section class="stats">
    <div class="container">
      <h2 class="section-title">Trusted by Thousands</h2>
      <p class="subtitle">We’ve helped many families find their dream homes.</p>
      <div class="stats-grid">
        <div class="stat-card" v-for="(stat, index) in stats" :key="index">
          <h3 class="stat-number">{{ stat.number }}</h3>
          <p class="stat-label">{{ stat.label }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const stats = [
  { number: "850+", label: "Properties Listed" },
  { number: "600+", label: "Happy Clients" },
  { number: "100+", label: "Professional Agents" },
  { number: "12+", label: "Years of Experience" },
];
</script>

<style scoped>
:root {
  --primary-color: #0B4251;
  --primary-light-color: #87BBD7;
  --secondary-color: #F2C864;
}

.stats {
  background: var(--primary-color);
  color: white;
  padding: 4rem 1.5rem;
  text-align: center;
}

.container {
  max-width: 1100px;
  margin: auto;
}

.section-title {
  font-size: 2rem;
  color: var(--secondary-color);
  margin-bottom: 0.5rem;
}

.subtitle {
  font-size: 1rem;
  color: #cfe4ea;
  margin-bottom: 2rem;
}

.stats-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  gap: 2rem;
}

.stat-card {
  background: rgba(255, 255, 255, 0.05);
  padding: 2rem 1rem;
  border-radius: 12px;
  transition: transform 0.3s;
}

.stat-card:hover {
  transform: translateY(-5px);
  background: rgba(255, 255, 255, 0.1);
}

.stat-number {
  font-size: 2rem;
  font-weight: bold;
  color: var(--secondary-color);
}

.stat-label {
  margin-top: 0.5rem;
  font-size: 1rem;
  color: #e2e2e2;
}
</style>
