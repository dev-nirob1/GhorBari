<template>
    <section class="featured bg-white">
        <div class="container large-2 align-center gap-2">
            <!-- Trust-building content -->
            <div>
                <!-- Section Title -->
                <h3 class="title">Luxury Duplex in Dhanmondi</h3>

                <p>
                    Discover this modern duplex in Dhanmondi, designed for elegant living with comfort, space, and
                    privacy in mind.
                </p>

                <ul>
                    <li>
                        <h5 class="sub-title">Lower Floor</h5>
                        <p>1 Bed, 2 Baths, Living, Dining, Kitchen & Open Terrace</p>
                    </li>
                    <li>
                        <h5 class="sub-title">Upper Floor</h5>
                        <p>3 Beds, 3 Baths, Family Lounge & 2 Balconies</p>
                    </li>
                    <li>
                        <h5 class="sub-title">Highlights</h5>
                        <p>4 Beds, 5 Baths, Private Parking & 24/7 Security</p>
                    </li>
                </ul>
            </div>

            <div class="image flex gap-1">
                <div class="flex flex-col gap-1">
                    <img src="https://cdn.pixabay.com/photo/2016/11/22/23/38/apartment-1851201_1280.jpg"
                        alt="Front view" />
                </div>
                <div class="flex flex-col gap-1">
                    <img src="https://cdn.pixabay.com/photo/2023/12/11/06/21/kitchen-8442907_640.jpg" alt="Kitchen" />
                    <img src="https://cdn.pixabay.com/photo/2023/12/30/07/31/living-room-8477525_1280.jpg"
                        alt="Living room" />
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped>
.featured {
    padding: 3.75rem 0;
}

.featured .title {
    margin-bottom: 1rem;
}

.featured ul {
    list-style: none;
    padding: 0;
    margin: 2rem 0;
}
.featured ul li {
    background-color: var(--white-color);
    border-radius: .75rem;
    padding: .5rem 0 .5rem 1rem;
    border-left: 2px solid var(--secondary-color);
    margin-bottom: 1rem;
}
.featured ul li p {
    margin-top: .5rem;
    margin-bottom: 0;
}

.featured i {
    font-size: 1.25rem;
    width: fit-content;
    height: fit-content;
    padding: 0.75rem;
    border-radius: 50%;
    color: var(--secondary-color);
    background-color: var(--primary-color);
}

.featured .quote {
    position: relative;
    background-color: rgb(from var(--primary-color) r g b/ 15%);
    width: 100%;
    padding: 1rem 1.5rem;
}

.featured .quote::before {
    position: absolute;
    content: "";
    top: 0;
    left: 0;
    height: 100%;
    width: 5px;
    background: var(--alternative-color);
}

.featured .image {
    width: 100%;
    height: 100%;
}

.featured .image img {
    width: 100%;
    height: 100%;
    display: block;
    object-fit: cover;
}

.featured .btn {
    border: 1px solid transparent;
    color: var(--white-color);
    background-color: var(--alternative-color);
    padding: 0.75rem 1.5rem;
    font-size: 1rem;
}
</style>