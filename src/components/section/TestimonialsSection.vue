<script setup>
import { ref } from 'vue';
import TestimonialCard from '../Widget/TestimonialCard.vue';
const reviews = ref([
    {
        "review": "Zems helped us digitize student records and automate class schedules. It’s now easier to focus on what matters most — teaching.",
        "name": "Emily Johnson",
        "image": "https://images.unsplash.com/photo-1573496359142-b8d87734a5a2",
        "description": "School Principal"
    },
    {
        "review": "Managing patient appointments and medical records has never been this smooth. Zems truly transformed our clinic operations.",
        "name": "Dr. Michael Chen",
        "image": "https://images.pexels.com/photos/5327585/pexels-photo-5327585.jpeg",
        "description": "Medical Director"
    }
])
</script>

<template>
    <section class="testimonials bg-light">
        <div class="container">
            <div class="mb-2">
                <BaseTitle class="text-center">What Our Clients Say</BaseTitle>
            </div>

            <div class="medium-2 gap-2">
                <TestimonialCard v-for="(review, i) in reviews" :key="i" :review="review" />
            </div>
        </div>
    </section>
</template>
<style scoped>
.testimonials {
    padding: 3.75rem 0;
}

.testimonials .sub-title {
    white-space: nowrap;
}

.testimonials .btn {
    padding: .5rem;
    white-space: nowrap;
}

@media (min-width: 768px) {
    .testimonials .btn {
        padding: .75rem 1rem;
    }
}
</style>