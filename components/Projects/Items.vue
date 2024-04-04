<script setup lang="ts">
const props = defineProps(['info'])
</script>

<template>
<div class="edu">
  <h3>{{props.info.project}}</h3>

  <h3>{{props.info.description}}</h3>
  <p v-for="tech in props.info.technology"><-{{tech}}</p>



</div>
</template>

<style scoped>
.edu {

  align-content: center;
  align-items: center;
}
</style>