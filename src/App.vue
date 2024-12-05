<script setup>
import { ref } from 'vue'
const buttons = ref([
  {
    value: 5,
    name: '5%',
  },
  { value: 10, name: '10%' },
  { value: 15, name: '15%' },
  { value: 25, name: '25%' },
  { value: 50, name: '50%' },
])
</script>

<template>
  <main>
    <div class="image-container">
      <img src="./assets/images/logo.svg" />
    </div>
    <div class="container">
      <div class="calculator">
        <div class="input-field">
          <span class="input-title">Bill</span>
          <div class="input">
            <img src="./assets/images/icon-dollar.svg" />
            <input type="text" />
          </div>
        </div>
        <div class="tip">
          <span>Select Tip %</span>
          <div class="select-tip">
            <button
              type="button"
              class="button"
              v-for="button in buttons"
              :key="button.value"
              :value="button.value"
            >
              <span> {{ button.name }}</span>
            </button>
            <input type="button" class="button-input" value="Custom" />
            <!-- <input type="text" class="button-input selected" value="" /> -->
          </div>
        </div>
        <div class="input-field">
          <span class="input-title">Number of People</span>
          <div class="input">
            <img src="./assets/images/icon-person.svg" />
            <input type="text" />
          </div>
        </div>
      </div>
      <div class="result"></div>
    </div>
  </main>
</template>

<style scoped></style>
