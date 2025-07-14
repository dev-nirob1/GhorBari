<template>
    <section class="news-letter">
        <div class="container content">
            <BaseTitle class="mb-1">NewsLetter Subscribe</BaseTitle>
            <div class="subscribe-form">
                <InputField placeholder="Enter Your Email"></InputField>
                <BaseButton>Subscribe</BaseButton>
            </div>
        </div>
    </section>
</template>
<style scoped>
.news-letter {
    padding: 3.75rem 0;
    text-align: center;
    color: var(--white-color);
    background:
        linear-gradient(rgba(11, 66, 81, 0.5),
            rgba(11, 66, 81, 0.5)),
        url('https://images.unsplash.com/photo-1600585154340-be6161a56a0c?auto=format&fit=crop&w=1650&q=80') center/cover no-repeat fixed;

}

.subscribe-form {
    width: 70%;
    margin: 0 auto;
    display: flex;
    justify-content: center;
}

.subscribe-form input {
    border-color: var(--alternative-color);
    outline: none;
    padding: 1.15rem;
    border-radius: 1rem 0 0 0;
}

.subscribe-form input::placeholder {
    color: var(--white-color);
    font-size: 1rem;
}

.subscribe-form .btn {
    background-color: var(--alternative-color);
    font-size: 1.25rem;
    font-weight: 500;
    border-radius: 0 0 1rem 0;
    padding: 1rem 3rem;
}
</style>