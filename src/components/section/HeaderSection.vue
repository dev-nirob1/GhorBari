<script setup>
import { onMounted, ref } from 'vue';

const isMenuOpen = ref(false)

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};

onMounted(() => {
  const navbar = document.querySelector('.nav-links')
  // console.log(navbar.childNodes);
  navbar.childNodes.forEach(element => {
    element.addEventListener('click', () => {
      isMenuOpen.value = false
    })
  });
})
</script>

<template>
  <header class="navbar">
    <nav class="flex justify-between align-center container">
      <!-- Mobile Menu Toggle Button -->
      <BaseButton class="hamburger" @click="toggleMenu">
        <i :class="isMenuOpen ? 'fas fa-xmark' : 'fas fa-bars'" class="fa-2xl"></i>
      </BaseButton>
      <!-- Logo -->
      <a href="/" class="logo">
        <div class="logo-icon">
          <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M3 21H21" stroke="currentColor" stroke-width="2" stroke-linecap="round" />
            <path d="M5 21V7C5 6.44772 5.44772 6 6 6H9" stroke="currentColor" stroke-width="2" stroke-linecap="round" />
            <path d="M19 21V11C19 10.4477 18.5523 10 18 10H15" stroke="currentColor" stroke-width="2"
              stroke-linecap="round" />
            <path d="M9 6V4C9 3.44772 9.44772 3 10 3H14C14.5523 3 15 3.44772 15 4V6" stroke="currentColor"
              stroke-width="2" />
            <path d="M9 14H15" stroke="currentColor" stroke-width="2" stroke-linecap="round" />
            <path d="M9 18H15" stroke="currentColor" stroke-width="2" stroke-linecap="round" />
          </svg>
        </div>
        <span class="logo-text">Prime<span>Estate</span></span>
      </a>

      <!-- Navigation Links -->
      <div class="flex align-center gap-1">
        <ul class="nav-links" :class="{ 'active': isMenuOpen }">
          <ListItem>
            <a href="#">Home</a>
          </ListItem>
          <ListItem>
            <a href="#about">About</a>
          </ListItem>
          <ListItem>
            <a href="#services">Services</a>
          </ListItem>
          <ListItem>
            <a href="#blogs">Blogs</a>
          </ListItem>
          <ListItem>
            <a href="#testimonials">Gallery</a>
          </ListItem>
        </ul>
      </div>
      <BaseButton class="bg-alternative">List Your Property</BaseButton>
    </nav>
  </header>
</template>

<style scoped>
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
  transition: all 0.3s ease;
}

.navbar .btn {
  border-radius: .75rem 0 .75rem 0;
}

/* Logo Styles */
.logo {
  display: flex;
  align-items: center;
  gap: 10px;
  text-decoration: none;
  font-weight: 700;
  font-size: 1.5rem;
  /* color: var(--white-color); */
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

.logo img {
  height: 55px;
  width: auto;
}

/* logo vissibility hidden/block */
.logo .desktop-logo {
  display: none;
}

.logo .mobile-logo {
  height: 55px;
  width: auto;
}

.nav-links {
  display: flex;
  align-items: center;
}

.navbar ul {
  list-style: none;
  position: fixed;
  top: -100%;
  left: -100%;
  width: 80%;
  margin: 0;
  background: var(--secondary-color);
  flex-direction: column;
  align-items: flex-start;
  padding: 2rem;
  gap: 1.5rem;
  transition: 0.3s;
}

.navbar ul.active {
  top: 5rem;
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

/* Mobile menu toggle */
.hamburger {
  display: block;
  color: var(--white-color);
  border: none;
  cursor: pointer;
}

@media (min-width: 992px) {
  .navbar ul {
    position: inherit;
    width: 100%;
    flex-direction: row;
    align-items: center;
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
    background: var(--secondary-color);
    transition: width 0.3s ease;
  }

  .navbar ul li a:hover::after {
    width: 100%;
  }

  /* logo vissibility hidden/block */
  .logo .desktop-logo {
    display: block;
  }

  .logo .mobile-logo {
    display: none;
  }

  .phone-num {
    border-left: 1px solid var(--secondary-color);
  }

  /* expand navlinks on desktop  */
  .hamburger {
    display: none;
  }
}
</style>