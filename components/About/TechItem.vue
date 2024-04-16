<script setup lang="ts">
import { defineProps, watchEffect, ref } from 'vue';

const props = defineProps(['items']);
const shuffledItems = ref([]);

watchEffect(() => {
  shuffledItems.value = props.items.sort(() => Math.random() - 0.5);
});
</script>

<template>
  <div>
    <div
        v-for="(tech, index) in shuffledItems"
        :key="index"
        class="tech"
        :style="{ animationDelay: `${index * 150}ms` }"
    >
      <span class="item">{{ tech }}</span>
    </div>
  </div>
</template>

<style scoped>
.tech-item {
  padding: 0.5rem;
  border-radius: 12px;
  margin-right: 0.8rem;
  color: #02d5fa;
  background-color: rgba(73, 152, 165, 0.25);
  cursor: pointer;
}

.tech {
  margin: 1rem 0;
  max-width: 15rem;
  display: inline-block;
  flex-direction: column;
  animation: fadeIn 0.7s ease backwards;
}

.tech .item {
  font-weight: bold;
  padding: 0.5rem;
  border-radius: 12px;
  font-size: 0.85rem;
  margin-right: 0.8rem;
  color: #02d5fa;
  background-color: rgba(73, 152, 165, 0.25);
}

.tech .tech-item:hover {
  padding: 0.2rem;
  border-radius: 10px;
  margin-right: 0.8rem;
  color: #4998a5;
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(-10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
