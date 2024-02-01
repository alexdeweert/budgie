<script setup lang="ts">
import { useCounterStore } from '@/stores/counter'
import { computed } from 'vue'
import { useRoute } from 'vue-router'

const route = useRoute()
const counterStore = useCounterStore()

let bar = route.query.bar

let count = computed(() => counterStore.count)

function handleClicked() {
  counterStore.increment()
}
</script>

<template>
  <div>
    <h1>Hello Home - {{ bar }} - {{ count }}</h1>
    <button @click="handleClicked()">Increment</button>
  </div>
</template>

<style></style>
