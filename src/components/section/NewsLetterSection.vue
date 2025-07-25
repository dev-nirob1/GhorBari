<template>
        <!-- ======== News-letter section ======== -->
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
        linear-gradient(to right, rgb(from var(--primary-color) r g b / 50%), rgb(from var(--primary-color) r g b / 50%)),
        url('https://images.unsplash.com/photo-1600585154340-be6161a56a0c?auto=format&fit=crop&w=1650&q=80') center/cover no-repeat fixed;
}

.news-letter .subscribe-form {
    width: 100%;
    margin: 0 auto;
    display: flex;
    justify-content: center;
}

.news-letter .subscribe-form input {
    color: var(--white-color);
    border-color: var(--secondary-color);
    outline: none;
    padding: 1.15rem;
    border-radius: 1rem 0 0 0;
    flex: 1;
}

.news-letter .subscribe-form input::placeholder {
    color: var(--white-color);
    font-size: 1rem;
}

.news-letter .subscribe-form .btn {
    background-color: var(--secondary-color);
    font-weight: 500;
    border-radius: 0 0 1rem 0;
    padding: 1rem;
}

@media (min-width: 768px) {
    .news-letter .subscribe-form {
        width: 70%;
    }

    .news-letter .subscribe-form .btn {
        font-size: 1.25rem;
        padding: 1rem 3rem;
    }
}
</style>