<template>
  <nav class="sidebar">
    <ul>
      <li v-for="(item, index) in sidebarItems" :key="index" @click="activateField(index)" :class="{ 'active': activeField === index }">
        {{ item.label }}
      </li>
    </ul>
  </nav>
</template>

<script setup>
import { ref } from 'vue';

const sidebarItems = ref([
  { label: 'Education', content: 'Content for Education' },
  { label: 'About', content: 'Content for About' },
  { label: 'Projects', content: 'Content for Projects' },
  { label: 'Skills', content: 'Content for Skills' }
]);

const activeField = ref(0);

const activateField = (index) => {
  activeField.value = index;
};


</script>

<style scoped>
.sidebar {
  width: 200px;
height:75vh;
  background-color: #031226;
  padding: 20px;
  display: flex;
  justify-content: center;

}

.sidebar ul {
  width: 95%;
  list-style: none;
  padding: 0;
}

.sidebar li {
  cursor: pointer;
  margin-bottom: 10px;
  padding: 10px;
  border-radius: 5px;

}

.sidebar li:hover {
  background-color: #b0b0b0;
}

.sidebar li.active {
  background-color: #999;
}
</style>
