<script setup>
import { onMounted, ref } from 'vue';

const isMenuOpen = ref(false)

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};

onMounted(() => {
  const navbar = document.querySelector('.navbar');
  const navLinks = document.querySelector('.nav-links')

  window.addEventListener('scroll', () => {
    if (window.scrollY > 10) {
      navbar.classList.add('scrolling');
    } else {
      navbar.classList.remove('scrolling');
    }
  });
  // console.log(navbar.childNodes);
  navLinks.childNodes.forEach(element => {
    element.addEventListener('click', () => {
      isMenuOpen.value = false
    })
  });
})
</script>

<template>
  <!-- ======== Navbar section ======== -->
  <header class="navbar">
    <nav class="flex justify-between align-center gap-1 container">
      <!-- Mobile Menu Toggle Button -->
      <BaseButton class="hamburger" @click="toggleMenu">
        <i :class="isMenuOpen ? 'fas fa-xmark' : 'fas fa-bars'" class="fa-2xl"></i>
      </BaseButton>
      <!-- Logo -->
      <a href="/" class="logo">
        <div class="logo-icon">
          <i class="fa-solid fa-map-location-dot"></i>
        </div>
        <span class="logo-text">Ghor<span>Bari</span></span>
      </a>
      <!-- Navigation Links -->
      <ul :class="{ 'active': isMenuOpen }">
        <ListItem>
          <a href="#">Home</a>
        </ListItem>
        <ListItem>
          <a href="#featured">Featured</a>
        </ListItem>
        <ListItem>
          <a href="#cities">Explore Cities</a>
        </ListItem>
        <ListItem>
          <a href="#properties">Properties</a>
        </ListItem>
        <ListItem>
          <a href="#testimonials">Testimonials</a>
        </ListItem>

        <ListItem class="btn-mobile">
          <BaseButton class="bg-alternative">List Your Property</BaseButton>
        </ListItem>
      </ul>
      <!-- Button to start property listing process -->
      <BaseButton class="btn-desktop bg-alternative">List Your Property</BaseButton>
    </nav>
  </header>
</template>

<style scoped>
/* background-color change on animation  */
.navbar.scrolling {
  background: var(--primary-color);
  transition: background-color 0.3s ease;
}

.navbar {
  backdrop-filter: blur(50px);
  color: var(--white-color);
  box-shadow: var(--box-shadow);
  padding: 0.75rem 0;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 999;
}

/* Logo Styles */
.logo {
  display: flex;
  align-items: center;
  gap: .25rem;
  font-weight: 700;
  font-size: 1.5rem;
  margin: 0;
}

.logo-icon {
  width: 32px;
  height: 32px;
  color: var(--alternative-color);
}

.logo-text span {
  color: var(--alternative-color);
}

.navbar a {
  text-decoration: none;
}

.navbar ul {
  display: flex;
  align-items: center;
}

.navbar ul {
  list-style: none;
  position: fixed;
  top: 5.25rem;
  left: -100%;
  width: 80%;
  margin: 0;
  background: var(--primary-color);
  flex-direction: column;
  align-items: flex-start;
  padding: 2rem;
  gap: 1.5rem;
  transition: all 0.3s ease-in-out;
}

.navbar ul.active {
  top: 5.25rem;
  left: 0;
  color: var(--white-color);
}

.navbar ul li a {
  position: relative;
  display: inline-block;
  font-weight: 500;
  transition: color 0.3s ease-in-out;
  padding: 0.5rem 0;
}

.navbar .btn {
  border-radius: .75rem 0 .75rem 0;
  color: var(--primary-color);
  white-space: nowrap
}

/* Mobile menu toggle */
.hamburger {
  display: block;
  color: var(--white-color) !important;
  border: none;
  cursor: pointer;
  height: 2.5rem;
  width: 2.5rem;
  display: flex;
  align-items: center;
  justify-content: center;
}

/* cta button hidden/vissible */
.btn-desktop {
  display: none;
}

.btn-mobile {
  display: block;
}

@media (min-width: 992px) {
  .navbar ul {
    position: inherit;
    width: 100%;
    flex-direction: row;
    justify-content: center;
    background-color: transparent;
    padding: 0.75rem 0;
  }

  /* Desktop menu hover effects */
  .navbar ul li a::after {
    content: "";
    position: absolute;
    bottom: 0;
    left: 0;
    width: 0;
    height: 2px;
    background: var(--alternative-color);
    transition: width 0.3s ease;
  }

  .navbar ul li a:hover::after {
    width: 100%;
  }

  /* expand navlinks on desktop  */
  .hamburger {
    display: none;
  }

  /* cta button hidden/vissible */
  .btn-desktop {
    display: block;
  }

  .btn-mobile {
    display: none;
  }
}
</style>