<script setup>
import AttributeItem from './components/AttributeItem.vue'
</script>

<template>
  <main>
    <div class="card">
      <div class="results l-flex has-large-space">
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

  .score {
    display: flex;
    justify-content: center;
    flex-direction: column;
    background: var(--circle-color);
    aspect-ratio: 1 / 1;
    width: 12rem;
    border-radius: 50%;
    margin-inline: auto;
  }

  span {
    display: block;
    font-size: var(--biggest-font-size);
    font-weight: var(--font-extra-bold);
    color: hsl(var(--neutral-white), 1);
    line-height: 1.2;
  }

  .remark {
    color: hsl(var(--neutral-white), 1);
    font-weight: var(--font-bold);
    font-size: var(--h2-font-size);
  }
}

.title {
  font-weight: var(--font-bold);
  font-size: var(--h3-font-size);
}
</style>
