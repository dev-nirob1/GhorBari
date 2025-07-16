<template>
      <!-- ======== Footer section ======== -->
   <footer class="footer">
  <div class="container medium-2 large-4 gap-2 py-2">
    <!-- Footer logo and social media links -->
    <div>
      <a href="#" class="logo">
        <div class="logo-icon">
          <i class="fa-solid fa-map-location-dot"></i>
        </div>
        <span class="logo-text">Ghor<span>Bari</span></span>
      </a>

      <p>Find your next home with trusted agents and verified listings.</p>
      <div class="social-links">
        <a href="#"><i class="fab fa-facebook-f"></i></a>
        <a href="#"><i class="fab fa-twitter"></i></a>
        <a href="#"><i class="fab fa-instagram"></i></a>
        <a href="#"><i class="fab fa-pinterest-p"></i></a>
      </div>
    </div>

    <!-- Quick navigation links -->
    <div>
      <h5 class="title">Quick Links</h5>
      <ul class="footer-links">
        <li><a href="/">Home</a></li>
        <li><a href="/properties">All Properties</a></li>
        <li><a href="/agents">Agents</a></li>
        <li><a href="/cities">Explore Cities</a></li>
        <li><a href="/blog">Blog</a></li>
      </ul>
    </div>

    <!-- Buying/Selling Information -->
    <div>
      <h5 class="title">Helpful Info</h5>
      <ul class="footer-links">
        <li><a href="/how-it-works">How It Works</a></li>
        <li><a href="/faq">FAQ</a></li>
        <li><a href="/terms">Terms of Service</a></li>
        <li><a href="/privacy">Privacy Policy</a></li>
        <li><a href="/contact">Contact Us</a></li>
      </ul>
    </div>

    <!-- Newsletter subscription form -->
    <div>
      <h5 class="title">Stay Updated</h5>
      <p>Subscribe to get the latest property listings and market tips.</p>
      <form class="subscribe-form">
        <input type="email" placeholder="Your email address" required />
        <button class="btn" type="submit">
          <i class="fas fa-paper-plane"></i>
        </button>
      </form>
    </div>
  </div>

  <!-- Footer bottom copyright -->
  <div class="footer-bottom">
    <p>© 2025 GhorBari. All rights reserved.</p>
  </div>
</footer>

</template>

<style scoped>
.footer {
    padding-top: 3rem;
    background-color: var(--primary-color);
    color: var(--white-color);
}

.footer h5 {
    margin-bottom: 1.5rem;
    position: relative;
    padding-bottom: 0.75rem;
}

/* Logo Styles */
.footer .logo {
    display: flex;
    align-items: center;
    gap: 10px;
    text-decoration: none;
    font-weight: 700;
    font-size: 1.5rem;
    color: var(--white-color);
}

.footer .logo-icon {
    width: 32px;
    height: 32px;
    color: var(--alternative-color);
}

.footer .logo-text span {
    color: var(--alternative-color);
}

.footer .social-links {
    display: flex;
    gap: 1rem;
}

/* Social links with hover effects */
.footer .social-links a {
    display: inline-block;
    text-decoration: none;
    font-size: 1.25rem;
    height: 36px;
    width: 36px;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: var(--alternative-color);
    color: var(--primary-color);
    border-radius: .5rem 0 .5rem 0;
}
.footer .footer-links a:hover{
    color: var(--alternative-color);
}
.footer .social-links a:hover i {
    transform: scale(1.2);
    transition: all 0.3s ease;
}

.footer h5::after {
    content: "";
    position: absolute;
    left: 0;
    bottom: 0;
    width: 4rem;
    height: 3px;
    background-color: var(--alternative-color);
}

.footer ul {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    flex-direction: column;
    gap: 1rem;
}

.footer ul a {
    text-decoration: none;
    transition: all 0.3s ease;
    display: flex;
    align-items: center;
    gap: 0.5rem;
}

.footer ul a::before {
    content: ">";
    font-family: monospace;
    color: var(--alternative-color);
    transition: all 0.3s ease;
}

/* Newsletter form */
.footer .subscribe-form {
    display: flex;
}

.footer .subscribe-form input {
    flex: 1;
    padding: 0.8rem 1.2rem;
    border: none;
    outline: none;
    border-radius: 1rem 0 0 0;
    font-size: 0.95rem;
    background-color: var(--white-color);
}

.footer .subscribe-form .btn {
    padding: 1rem 2rem;
    background-color: var(--alternative-color);
    color: var(--primary-color);
    border: none;
    border-radius: 0 0 1rem 0;
}

/* Footer copyright bar*/
.footer .footer-bottom {
    padding: .5rem;
    border-top: var(--white-color);
    text-align: center;
    background-color: rgb(from var(--alternative-color)r g b / 5%);
}
</style>