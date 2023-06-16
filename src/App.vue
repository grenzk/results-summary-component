<script setup>
import attributeData from '@/data.json'
import { AttributeItem } from '@/components'
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

      <div class="summary l-flex has-large-space">
        <h1 class="title">Summary</h1>

        <div class="l-flex">
          <template v-for="item in attributeData" :key="item.id">
            <AttributeItem
              :name="item.category"
              :color="item.color"
              :rating="item.score"
              :icon-name="item.icon"
            />
          </template>
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

.summary {
  padding: 2.5rem;

  .attribute-item {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: hsl(var(--attribute-item-color), 0.1);
    padding: 1rem;
    border-radius: 0.5rem;

    .name {
      color: hsl(var(--attribute-item-color));
      font-weight: var(--font-bold);
    }
  }

  .attribute-item.is-light-red {
    --attribute-item-color: var(--primary-light-red);
  }
  .attribute-item.is-orangey-yellow {
    --attribute-item-color: var(--primary-orangey-yellow);
  }
  .attribute-item.is-green-teal {
    --attribute-item-color: var(--primary-green-teal);
  }
  .attribute-item.is-cobalt-blue {
    --attribute-item-color: var(--primary-cobalt-blue);
  }

  .rating {
    color: hsl(var(--neutral-dark-gray-blue), 0.5);
    font-weight: var(--font-extra-bold);

    span {
      color: hsl(var(--neutral-dark-gray-blue));
    }
  }

  .button {
    color: hsl(var(--neutral-white));
    background: hsl(var(--neutral-dark-gray-blue));
    padding: 0.8rem 2rem;
    border: none;
    border-radius: 100vw;
    cursor: pointer;

    &:hover,
    &:focus-visible {
      background: var(--background-color);
    }
  }
}
</style>
