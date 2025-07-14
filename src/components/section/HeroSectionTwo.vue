<!-- HeroSection.vue -->
<template>
  <section class="hero">
    <div class="overlay">
      <div class="content">
        <p class="tagline">🏠 Your Perfect Home Awaits</p>
        <h1 class="title">
          Find Real Estate<br />That Matches <span>You</span>
        </h1>
        <p class="description">
          Explore premium properties in your favorite neighborhoods with trusted agents.
        </p>
        <div class="actions">
          <button class="primary-btn">Browse Properties</button>
          <button class="secondary-btn">Contact Agent</button>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero {
  background: url('https://images.unsplash.com/photo-1600585154340-be6161a56a0c?auto=format&fit=crop&w=1650&q=80') center/cover no-repeat;
  min-height: 100vh;
  position: relative;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
}

.overlay {
  background: rgba(11, 66, 81, 0.7); /* semi-transparent overlay */
  position: absolute;
  inset: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 2rem;
}

.content {
  max-width: 80%;
  text-align: center;
  padding-top: 5rem;

}

.tagline {
  font-size: 1.2rem;
  color: var(--secondary-color);
  margin-bottom: 0.5rem;
  font-weight: 600;
  letter-spacing: 1px;
}

.title {
  font-size: 3rem;
  font-weight: bold;
  line-height: 1.3;
}

.title span {
  color: var(--secondary-color);
}

.description {
  font-size: 1.1rem;
  margin-top: 1rem;
  margin-bottom: 2rem;
  color: #f0f0f0;
}

.actions {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
  justify-content: center;
}

.primary-btn {
  background-color: var(--secondary-color);
  color: var(--primary-color);
  padding: 0.75rem 1.5rem;
  border: none;
  border-radius: 6px;
  font-weight: 600;
  cursor: pointer;
  transition: background 0.3s;
}

.primary-btn:hover {
  background-color: var(--primary-light-color);
}

.secondary-btn {
  background: transparent;
  border: 2px solid var(--secondary-color);
  color: var(--secondary-color);
  padding: 0.75rem 1.5rem;
  border-radius: 6px;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s;
}

.secondary-btn:hover {
  background-color: var(--secondary-color);
  color: var(--primary-color);
}
</style>
