<template>
      <!-- ======== Statistics section ======== -->
  <section class="bg-white statistics">
    <div class="container">
      <ul class="small-2 larger-3 justify-center align-center gap-2">
        <!-- Properties Listed -->
        <ListItem>
          <i class="fa-solid fa-building fa-2x"></i>
          <div>
            <BaseTitle>850+</BaseTitle>
            <BaseParagraph>Properties Listed</BaseParagraph>
          </div>
        </ListItem>

        <!-- Happy Clients -->
        <ListItem>
          <i class="fa-solid fa-user-check fa-2x"></i>
          <div>
            <BaseTitle>600+</BaseTitle>
            <BaseParagraph>Happy Clients</BaseParagraph>
          </div>
        </ListItem>

        <!-- Years of Experience -->
        <ListItem>
          <i class="fa-solid fa-calendar-check fa-2x"></i>
          <div>
            <BaseTitle>12+</BaseTitle>
            <BaseParagraph>Years of Excellence</BaseParagraph>
          </div>
        </ListItem>
      </ul>
    </div>
  </section>
</template>
<style scoped>
.statistics {
  padding: 3.75rem 0;
}

.statistics ul li {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 1rem;
  padding: 2rem .5rem;
  border: 1px solid var(--secondary-color);
  border-radius: 2rem 0;
}
.statistics ul i {
  height: 80px;
  width: 80px;
  line-height: 80px;
  text-align: center;
  border-radius: 50%;
  border: 1px dashed var(--secondary-color);
  color: var(--secondary-color);
}
.statistics ul p {
  margin: 0;
}
</style>
