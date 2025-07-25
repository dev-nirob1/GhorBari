<template>
          <!-- ======== Featured Project section ======== -->
    <section id="featured" class="featured bg-white">
        <div class="container large-2 align-center gap-2">
                  <!-- ======== Porject information section ======== -->
            <div>
                <BaseTitle class="mb-1">Luxury Duplex in Dhanmondi</BaseTitle>
                <BaseParagraph>
                    Discover this modern duplex in Dhanmondi, designed for elegant living with comfort, space, and
                    privacy in mind.
                </BaseParagraph>
                <ul>
                    <ListItem>
                        <SubTitle>Lower Floor</SubTitle>
                        <BaseParagraph>1 Bed, 2 Baths, Living, Dining, Kitchen & Open Terrace</BaseParagraph>
                    </ListItem>
                    <ListItem>
                        <SubTitle>Upper Floor</SubTitle>
                        <BaseParagraph>3 Beds, 3 Baths, Family Lounge & 2 Balconies</BaseParagraph>
                    </ListItem>
                    <ListItem>
                        <SubTitle>Highlights</SubTitle>
                        <BaseParagraph>4 Beds, 5 Baths, Private Parking & 24/7 Security</BaseParagraph>
                    </ListItem>
                </ul>
            </div>

                  <!-- ======== Porject images section ======== -->
            <div class="image-container flex gap-1">
                <div class="flex flex-col gap-1">
                    <BaseImage image="https://cdn.pixabay.com/photo/2023/12/11/06/21/kitchen-8442907_640.jpg"
                        alt="Kitchen" />
                    <BaseImage image="https://cdn.pixabay.com/photo/2023/12/30/07/31/living-room-8477525_1280.jpg"
                        alt="Living room" />
                </div>
                <div>
                    <BaseImage image="https://cdn.pixabay.com/photo/2016/11/22/23/38/apartment-1851201_1280.jpg"
                        alt="Front view" />
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped>
.featured {
    padding: 3.75rem 0;
}

.featured ul {
    margin: 2rem 0;
}

.featured ul li {
    background-color: var(--white-color);
    border-radius: .75rem;
    padding: .5rem 0 .5rem 1rem;
    border-left: 2px solid var(--alternative-color);
    margin-bottom: 1rem;
}

.featured ul li p {
    margin-top: .5rem;
    margin-bottom: 0;
}

.featured .image-container {
    width: 100%;
    height: 100%;
}

.featured .image-container img {
    width: 100%;
    height: 100%;
    display: block;
    object-fit: cover;
}
</style>