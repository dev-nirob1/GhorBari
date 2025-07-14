<template>
  <section class="bg-white statistics">
    <div class="container">
      <ul class="small-2 larger-4 gap-2 stats-content">
        <!-- Properties Listed -->
        <li>
          <i class="fa-solid fa-building fa-2x"></i>
          <div>
            <h3>850+</h3>
            <p>Properties Listed</p>
          </div>
        </li>

        <!-- Happy Clients -->
        <li>
          <i class="fa-solid fa-user-check fa-2x"></i>
          <div>
            <h3>600+</h3>
            <p>Happy Clients</p>
          </div>
        </li>

        <!-- Professional Agents -->
        <li>
          <i class="fa-solid fa-user-tie fa-2x"></i>
          <div>
            <h3>100+</h3>
            <p>Expert Agents</p>
          </div>
        </li>

        <!-- Years of Experience -->
        <li>
          <i class="fa-solid fa-calendar-check fa-2x"></i>
          <div>
            <h3>12+</h3>
            <p>Years of Excellence</p>
          </div>
        </li>
      </ul>
    </div>
  </section>
</template>

<script setup>
const stats = [
  { number: "850+", label: "Properties Listed" },
  { number: "600+", label: "Happy Clients" },
  { number: "100+", label: "Professional Agents" },
  { number: "12+", label: "Years of Experience" },
];
</script>

<style scoped>
.statistics {
  padding: 3.75rem 0;
}
.statistics .stats-content {
  list-style: none;
  padding: 0;
  height: 100%;
  align-items: center;
}
.statistics .stats-content li {
  display: flex;
  align-items: center;
  gap: .5rem;
  padding: 2rem .5rem;
  /* background-color: var(--primary-color); */
  border: 1px solid var(--secondary-color);
  border-radius: 2rem 0 2rem 0;
}
.statistics .stats-content i {
  height: 80px;
  width: 80px;
  line-height: 80px;
  text-align: center;
  border-radius: 50%;
  border: 2px dashed var(--secondary-color);
  color: var(--secondary-color);
}
.statistics .stats-content p {
  margin: 0;
}
</style>
