<template>
    <section class="hero">
        <div class="overlaping">
            <div class="content">
                <SubTitle> <i class="fa-solid fa-home"></i> Your Perfect Home</SubTitle>
                <HeroTitle>Your Dream Home Awaits</HeroTitle>
                <BaseParagraph>
                    Browse top properties in prime locations with guidance from verified agents. Find a place that truly
                    fits your lifestyle.
                </BaseParagraph>
                <div class="flex justify-center gap-1">
                    <BaseButton class="bg-primary">Browse Properties</BaseButton>
                    <BaseButton class="bg-alternative">Learn More</BaseButton>
                </div>
            </div>
        </div>
    </section>
</template>
<style scoped>
.hero {
    min-height: 100vh;
    text-align: center;
    background: url('https://images.unsplash.com/photo-1600585154340-be6161a56a0c?auto=format&fit=crop&w=1650&q=80') center/cover no-repeat;
    color: var(--white-color);
    position: relative;
}

.hero .overlaping {
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(to right, rgb(from var(--primary-color)r g b / 35%), rgb(from var(--primary-color)r g b / 55%), rgb(from var(--primary-color)r g b / 35%));
    display: flex;
    justify-content: center;
    align-items: center;
    padding-top: 6rem;

}

.content .sub-title i {
    color: var(--alternative-color);
}

.content .btn {
    padding: .75rem 1rem;
    font-size: .75rem;
    color: var(--white-color);
    border-radius: 1rem 0 1rem 0;
}

.content .bg-alternative.btn {
    color: var(--primary-color);
}

@media (min-width: 768px) {
    .content .btn {
        padding: 1.25rem 2rem;
        font-size: 1.25rem;
    }

    .content {
        max-width: 70%;
    }

    .content p {
        font-size: 1.15rem;
    }
}
</style>