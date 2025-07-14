<template>
    <footer class="footer">
        <div class="container medium-2 large-4 gap-2 pb-2">
            <!-- Company logo and description -->
            <div class="medium-span-2">
                <a href="/" class="logo">
                    <div class="logo-icon">
                        <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M3 21H21" stroke="currentColor" stroke-width="2" stroke-linecap="round" />
                            <path d="M5 21V7C5 6.44772 5.44772 6 6 6H9" stroke="currentColor" stroke-width="2"
                                stroke-linecap="round" />
                            <path d="M19 21V11C19 10.4477 18.5523 10 18 10H15" stroke="currentColor" stroke-width="2"
                                stroke-linecap="round" />
                            <path d="M9 6V4C9 3.44772 9.44772 3 10 3H14C14.5523 3 15 3.44772 15 4V6"
                                stroke="currentColor" stroke-width="2" />
                            <path d="M9 14H15" stroke="currentColor" stroke-width="2" stroke-linecap="round" />
                            <path d="M9 18H15" stroke="currentColor" stroke-width="2" stroke-linecap="round" />
                        </svg>
                    </div>
                    <span class="logo-text">Prime<span>Estate</span></span>
                </a>
                <BaseParagraph>
                    Zems delivers next-generation software solutions, helping startups and enterprises across Ireland
                    and beyond
                    accelerate digital transformation, boost productivity, and scale with confidence.
                </BaseParagraph>
                <div class="social-links">
                    <a href="/"><i class="fab fa-linkedin-in"></i></a>
                    <a href="/"><i class="fab fa-twitter"></i></a>
                    <a href="/"><i class="fab fa-github"></i></a>
                    <a href="/"><i class="fab fa-facebook-f"></i></a>
                </div>
            </div>
            <!-- Company information links -->
            <div>
                <SubTitle>Company</SubTitle>
                <ul class="footer-links">
                    <ListItem>
                        <a href="/">About Us</a>
                    </ListItem>
                    <ListItem>
                        <a href="/">Careers</a>
                    </ListItem>
                    <ListItem>
                        <a href="/">Case Studies</a>
                    </ListItem>
                    <ListItem>
                        <a href="/">Privacy Policy</a>
                    </ListItem>
                    <ListItem>
                        <a href="/">Contact Us</a>
                    </ListItem>
                </ul>
            </div>
            <!-- Newsletter subscription form -->
            <div>
                <h5 class="title">Stay Updated</h5>
                <BaseParagraph>Subscribe to our newsletter for tech insights and company news</BaseParagraph>
                <form class="subscribe-form">
                    <InputField type="email" placeholder="Your email address" required />
                    <BaseButton type="submit">
                        <i class="fas fa-paper-plane"></i>
                    </BaseButton>
                </form>
            </div>
        </div>
        <!-- Footer bottom copyright with Irish location -->
        <div class="footer-bottom">
            <p>© 2025 Zems. All rights reserved. Registered in Ireland.</p>
        </div>
    </footer>
</template>

<style scoped>
.footer {
    padding-top: 5rem;
    background-color: var(--primary-color);
    color: var(--white-color);
}

.footer h5 {
    margin-bottom: 1.5rem;
    position: relative;
    padding-bottom: 0.75rem;
}
/* Logo Styles */
.logo {
  display: flex;
  align-items: center;
  gap: 10px;
  text-decoration: none;
  font-weight: 700;
  font-size: 1.5rem;
  color: var(--white-color);
}

.logo-icon {
  width: 32px;
  height: 32px;
  color: var(--secondary-color);
}

.logo-text span {
  color: var(--primary-light-color);
}
/* .footer .logo {
    display: flex;
    align-items: center;
    font-size: 1.5rem;
    text-decoration: none;
}

.footer .logo img {
    height: 55px;
    width: auto;
} */

.social-links {
    display: flex;
    gap: 1rem;
}

/* Social links with hover effects */
.social-links a {
    display: inline-block;
    text-decoration: none;
    font-size: 1.25rem;
    height: 36px;
    width: 36px;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: var(--secondary-color);
    color: var(--white-color);
}

.social-links a:hover i {
    transform: scale(1.2);
    transition: all 0.3s ease;
}

.footer h5::after {
    content: "";
    position: absolute;
    left: 0;
    bottom: 0;
    width: 70px;
    height: 3px;
    background-color: var(--white-color);
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
    content: "→";
    /* color: var(--primary-light-color); */
    opacity: 0;
    display: none;
    transition: all 0.3s ease;
}

.footer ul a:hover {
    padding-left: 5px;
}

.footer ul a:hover::before {
    opacity: 1;
    display: block;
}

/* Newsletter form */
.subscribe-form {
    display: flex;
}

.subscribe-form input {
    flex: 1;
    padding: 0.8rem 1.2rem;
    border: none;
    outline: none;
    font-size: 0.95rem;
    background-color: var(--white-color);
}

.subscribe-form .btn {
    padding: 1rem 2rem;
    background-color: var(--secondary-color);
    color: var(--white-color);
    border: none;
}

/* Footer copyright bar*/
.footer-bottom {
    padding: 1rem;
    border-top: var(--white-color);
    text-align: center;
    background-color: rgb(from var(--primary-color)r g b / 10%);
}
</style>