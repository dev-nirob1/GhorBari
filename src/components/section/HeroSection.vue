<template>
    <section class="hero">
        <div class="overlaping">
            <div class="content">
                <SubTitle> <i class="fa-solid fa-home"></i> Your Perfect Home</SubTitle>
                <HeroTitle>Find Real Estate</HeroTitle>
                <HeroTitle>That Matches You</HeroTitle>
                <BaseParagraph>
                    Explore premium properties in your favorite neighborhoods with trusted agents.
                </BaseParagraph>
                <div class="flex justify-center gap-1">
                    <BaseButton>Browse Properties</BaseButton>
                    <BaseButton>Learn More</BaseButton>
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
    display: flex;
    align-items: center;
    justify-content: center;
}

.hero .overlaping {
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background: rgb(from var(--primary-color)r g b / 25%);
    display: flex;
    justify-content: center;
    align-items: center;
}
.content .btn{
    padding: 1.25rem 2rem;
    font-size: 1.25rem;
    color: var(--white-color);
    border-radius: 1rem 0 1rem 0 ;
    background-color: var(--primary-color);
}
</style>