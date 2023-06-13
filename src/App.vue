<script setup>
import AttributeItem from './components/AttributeItem.vue'
</script>

<template>
  <main>
    <div class="card">
      <div class="results">
        <h1 class="title">Your Result</h1>

        <p class="score"><span>76</span>of 100</p>

        <div class="l-flex">
          <p class="remark">Great</p>
          <p>You scored higher than 65% of the people who have taken these tests.</p>
        </div>
      </div>

      <div class="summary">
        <h1 class="title">Summary</h1>

        <div class="l-flex">
          <AttributeItem />
          <AttributeItem />
          <AttributeItem />
          <AttributeItem />
        </div>

        <button class="button">Continue</button>
      </div>
    </div>
  </main>
</template>

<style lang="scss">
.card {
  display: flex;
  max-width: 46rem;
  flex-direction: column;
}

.results {
  background: var(--background-color);
  color: hsl(var(--neutral-white), 0.7);
  text-align: center;
  padding: 2.5rem calc(2.5rem * 1.5);
  border-radius: 0 0 2rem 2rem;

  
}
</style>
