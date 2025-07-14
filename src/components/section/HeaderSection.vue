<script setup>
import { ref, onMounted } from 'vue';

const isMenuOpen = ref(false);
const isScrolled = ref(false);

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
  document.body.style.overflow = isMenuOpen.value ? 'hidden' : '';
};

const closeMenu = () => {
  isMenuOpen.value = false;
  document.body.style.overflow = '';
};

onMounted(() => {
  // Handle scroll effect
  window.addEventListener('scroll', () => {
    isScrolled.value = window.scrollY > 10;
  });

  // Close menu when clicking on nav links
  const navLinks = document.querySelectorAll('.nav-link');
  navLinks.forEach(link => {
    link.addEventListener('click', closeMenu);
  });

  // Close menu on Escape key
  document.addEventListener('keydown', (e) => {
    if (e.key === 'Escape') closeMenu();
  });
});
</script>

<template>
  <header 
    class="navbar" 
    :class="{ 'scrolled': isScrolled, 'menu-open': isMenuOpen }"
  >
    <div class="container">
      <nav class="nav-container">
        <!-- Logo -->
        <a href="/" class="logo">
          <div class="logo-icon">
            <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M3 21H21" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
              <path d="M5 21V7C5 6.44772 5.44772 6 6 6H9" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
              <path d="M19 21V11C19 10.4477 18.5523 10 18 10H15" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
              <path d="M9 6V4C9 3.44772 9.44772 3 10 3H14C14.5523 3 15 3.44772 15 4V6" stroke="currentColor" stroke-width="2"/>
              <path d="M9 14H15" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
              <path d="M9 18H15" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
            </svg>
          </div>
          <span class="logo-text">Prime<span>Estate</span></span>
        </a>

        <!-- Desktop Navigation -->
        <ul class="nav-links">
          <li><a href="/" class="nav-link">Home</a></li>
          <li><a href="/properties" class="nav-link">Properties</a></li>
          <li><a href="/agents" class="nav-link">Agents</a></li>
          <li><a href="/about" class="nav-link">About</a></li>
          <li><a href="/contact" class="nav-link">Contact</a></li>
        </ul>

        <!-- CTA Buttons -->
        <div class="nav-actions">
          <a href="/login" class="login-btn">Sign In</a>
          <a href="/list-property" class="cta-btn">List Your Property</a>
        </div>

        <!-- Mobile Menu Toggle -->
        <button 
          class="hamburger" 
          @click="toggleMenu"
          aria-label="Toggle navigation"
          :aria-expanded="isMenuOpen"
        >
          <span class="hamburger-line" :class="{ 'open': isMenuOpen }"></span>
          <span class="hamburger-line" :class="{ 'open': isMenuOpen }"></span>
          <span class="hamburger-line" :class="{ 'open': isMenuOpen }"></span>
        </button>
      </nav>
    </div>

    <!-- Mobile Menu -->
    <div class="mobile-menu" :class="{ 'open': isMenuOpen }">
      <div class="mobile-menu-content">
        <ul>
          <li><a href="/" class="mobile-nav-link">Home</a></li>
          <li><a href="/properties" class="mobile-nav-link">Properties</a></li>
          <li><a href="/agents" class="mobile-nav-link">Agents</a></li>
          <li><a href="/about" class="mobile-nav-link">About</a></li>
          <li><a href="/contact" class="mobile-nav-link">Contact</a></li>
        </ul>
        <div class="mobile-actions">
          <a href="/login" class="mobile-login-btn">Sign In</a>
          <a href="/list-property" class="mobile-cta-btn">List Your Property</a>
        </div>
      </div>
    </div>
  </header>
</template>

<style scoped>
/* Base Styles */
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1000;
  transition: all 0.3s ease;
  background-color: rgba(255, 255, 255, 0.9);
  backdrop-filter: blur(10px);
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
}

.navbar.scrolled {
  background-color: rgba(11, 66, 81, 0.95);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

.nav-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 80px;
}

/* Logo Styles */
.logo {
  display: flex;
  align-items: center;
  gap: 10px;
  text-decoration: none;
  font-weight: 700;
  font-size: 1.5rem;
  color: var(--primary-color);
}

.logo-icon {
  width: 32px;
  height: 32px;
  color: var(--secondary-color);
}

.logo-text span {
  color: var(--secondary-color);
}

.navbar.scrolled .logo {
  color: white;
}

.navbar.scrolled .logo-text span {
  color: var(--primary-light-color);
}

/* Desktop Navigation */
.nav-links {
  display: flex;
  gap: 30px;
  list-style: none;
}

.nav-link {
  position: relative;
  text-decoration: none;
  color: var(--primary-color);
  font-weight: 500;
  transition: color 0.3s ease;
  padding: 8px 0;
}

.navbar.scrolled .nav-link {
  color: white;
}

.nav-link::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 2px;
  background-color: var(--secondary-color);
  transition: width 0.3s ease;
}

.nav-link:hover::after,
.nav-link.router-link-active::after {
  width: 100%;
}

.nav-link:hover {
  color: var(--secondary-color);
}

.navbar.scrolled .nav-link:hover {
  color: var(--primary-light-color);
}

/* CTA Buttons */
.nav-actions {
  display: flex;
  align-items: center;
  gap: 15px;
}

.login-btn {
  padding: 8px 16px;
  border-radius: 4px;
  text-decoration: none;
  color: var(--primary-color);
  font-weight: 500;
  transition: all 0.3s ease;
}

.navbar.scrolled .login-btn {
  color: white;
}

.login-btn:hover {
  color: var(--secondary-color);
}

.navbar.scrolled .login-btn:hover {
  color: var(--primary-light-color);
}

.cta-btn {
  padding: 10px 20px;
  background-color: var(--secondary-color);
  color: var(--primary-color);
  border-radius: 4px;
  text-decoration: none;
  font-weight: 600;
  transition: all 0.3s ease;
}

.cta-btn:hover {
  background-color: var(--primary-light-color);
  transform: translateY(-2px);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.navbar.scrolled .cta-btn {
  background-color: var(--primary-light-color);
  color: var(--primary-color);
}

.navbar.scrolled .cta-btn:hover {
  background-color: white;
}

/* Hamburger Menu */
.hamburger {
  display: none;
  background: none;
  border: none;
  cursor: pointer;
  padding: 10px;
  z-index: 1001;
}

.hamburger-line {
  display: block;
  width: 25px;
  height: 2px;
  background-color: var(--primary-color);
  margin: 5px 0;
  transition: all 0.3s ease;
}

.navbar.scrolled .hamburger-line {
  background-color: white;
}

.hamburger-line.open:nth-child(1) {
  transform: translateY(7px) rotate(45deg);
}

.hamburger-line.open:nth-child(2) {
  opacity: 0;
}

.hamburger-line.open:nth-child(3) {
  transform: translateY(-7px) rotate(-45deg);
}

/* Mobile Menu */
.mobile-menu {
  position: fixed;
  top: 80px;
  left: 0;
  width: 100%;
  height: calc(100vh - 80px);
  background-color: var(--primary-color);
  transform: translateX(100%);
  transition: transform 0.3s ease;
  z-index: 999;
  overflow-y: auto;
}

.mobile-menu.open {
  transform: translateX(0);
}

.mobile-menu-content {
  padding: 30px;
  display: flex;
  flex-direction: column;
  height: 100%;
}

.mobile-menu ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.mobile-menu li {
  margin-bottom: 20px;
}

.mobile-nav-link {
  color: white;
  text-decoration: none;
  font-size: 1.2rem;
  font-weight: 500;
  transition: color 0.3s ease;
  display: block;
  padding: 10px 0;
}

.mobile-nav-link:hover,
.mobile-nav-link.router-link-active {
  color: var(--secondary-color);
}

.mobile-actions {
  margin-top: auto;
  display: flex;
  flex-direction: column;
  gap: 15px;
  padding: 20px 0;
}

.mobile-login-btn {
  padding: 12px;
  text-align: center;
  border-radius: 4px;
  text-decoration: none;
  color: white;
  font-weight: 500;
  border: 1px solid white;
  transition: all 0.3s ease;
}

.mobile-login-btn:hover {
  background-color: rgba(255, 255, 255, 0.1);
}

.mobile-cta-btn {
  padding: 12px;
  background-color: var(--secondary-color);
  color: var(--primary-color);
  border-radius: 4px;
  text-decoration: none;
  font-weight: 600;
  text-align: center;
  transition: all 0.3s ease;
}

.mobile-cta-btn:hover {
  background-color: var(--primary-light-color);
  transform: translateY(-2px);
}

/* Responsive Styles */
@media (max-width: 992px) {
  .nav-links,
  .nav-actions {
    display: none;
  }

  .hamburger {
    display: block;
  }
}

@media (max-width: 576px) {
  .nav-container {
    height: 70px;
  }

  .mobile-menu {
    top: 70px;
    height: calc(100vh - 70px);
  }
}
</style>