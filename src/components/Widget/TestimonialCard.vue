<script setup>
defineProps({
  review: {
    type: Object
  }
})
</script>

<template>
  <div class="testimonial-card">
    <i class="bg-graphic fa-solid fa-quote-right fa-10x"></i>
        <div class="flex align-center gap-1">
      <BaseImage class="height-full width-full" :image="review.image" :alt="review.description" />
      <div>
        <SubTitle>{{ review.name }}</SubTitle>
        <span>{{ review.description }}</span>
      </div>
    </div>
    <div class="flex">
      <BaseParagraph>
        <i class="fa-solid fa-quote-left fa-2x"></i>
        {{ review.review }}
      </BaseParagraph>
    </div>

  </div>
</template>

<style>
.testimonial-card {
  position: relative;
  padding: 2rem 1.5rem;
  background: var(--white-color);
  box-shadow: var(--box-shadow);
  scroll-snap-align: start;
  border-radius: 3rem 0 3rem 0;
}

.testimonial-card img {
  height: 4rem;
  width: 4rem;
  object-fit: cover;
  border-radius: 1rem 0 1rem 0;
}

.bg-graphic {
  position: absolute;
  right: 1rem;
  top: 0;
  opacity: .1;
}


@media (min-width: 992px) {

  .testimonial-card p,
  .testimonial-card span {
    font-size: 1.15rem;
  }

  .bg-graphic {
    right: 2rem;
    bottom: 0;
  }
}
</style>