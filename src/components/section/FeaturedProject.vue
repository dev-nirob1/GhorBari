<template>
    <section class="about-us bg-white">
        <div class="container large-2 align-center gap-2">

            <!-- trust-building content -->
            <div>
                <!-- Section Title -->
                <h3 class="title">Featured Project</h3>
                <!-- Section Description -->
                <p>
                    We help over 500,000 shoppers save money daily, offering exclusive
                    deals in more than 70 countries. Our global reach ensures you get
                    the best discounts, anytime, anywhere.
                </p>
                <!-- Feature Icons List -->
                <ul class="">
                    <li>
                        <div>
                            <h5 class="sub-title">DUPLEX FLOOR (LOWER Floor)</h5>
                            <p>1 Bed, 2 Baths (1 Attached & 1 Common), 1 Ver, Formal Living, Dining, Kitchen with Verand
                                & Open Terrace.</p>
                        </div>
                    </li>
                    <li>
                        <div>
                            <h5 class="sub-title">DUPLEX FLOOR (UPPER Floor)</h5>
                            <p>3 Beds, 3 Baths (2 Attached & 1 Common), 2 Veranda & Family Living</p>
                        </div>
                    </li>
                    <li>
                        <div>
                            <h5 class="sub-title">Surmise</h5>
                            <p>4 Beds, 5 Baths, 3 Verandas, 2 Formal Living, Dining, Kitchen with Veranda and Open
                                Terrace.</p>
                        </div>
                    </li>
                </ul>
            </div>
            <!-- About Image -->
            <div class="image medium-2 gap-1">
                <div class="flex flex-col gap-1">
                    <img class="height-full"
                        src="https://images.unsplash.com/photo-1600585154340-be6161a56a0c?auto=format&fit=crop&w=1650&q=80"
                        alt="image" /><img class="height-full"
                        src="https://images.unsplash.com/photo-1600585154340-be6161a56a0c?auto=format&fit=crop&w=1650&q=80"
                        alt="image" />
                </div>
                <div class="flex flex-col gap-1">
                    <img src="https://images.unsplash.com/photo-1600585154340-be6161a56a0c?auto=format&fit=crop&w=1650&q=80"
                        alt="image" />
                    <img src="https://images.unsplash.com/photo-1600585154340-be6161a56a0c?auto=format&fit=crop&w=1650&q=80"
                        alt="image" />
                </div>
            </div>
        </div>
    </section>
</template>
<style scoped>
.about-us {
    padding: 3.75rem 0;
}

.about-us .title {
    margin-bottom: 1rem;
}

.about-us ul {
    list-style: none;
    padding: 0;
    margin: 2rem 0;
}

.about-us ul li {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
}

.about-us i {
    font-size: 1.25rem;
    width: fit-content;
    height: fit-content;
    padding: 0.75rem;
    border-radius: 50%;
    color: var(--secondary-color);
    background-color: var(--primary-color);
}

.about-us .quote {
    position: relative;
    background-color: rgb(from var(--primary-color) r g b/ 15%);
    width: 100%;
    padding: 1rem 1.5rem;
}

.about-us .quote::before {
    position: absolute;
    content: "";
    top: 0;
    left: 0;
    height: 100%;
    width: 5px;
    background: var(--alternative-color);
}

.about-us .image {
    width: 100%;
}

.about-us .image img {
    width: 100%;
    height: auto;
    display: block;
}

.about-us .btn {
    border: 1px solid transparent;
    color: var(--white-color);
    background-color: var(--alternative-color);
    padding: 0.75rem 1.5rem;
    font-size: 1rem;
}
</style>