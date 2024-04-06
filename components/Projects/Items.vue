<script setup lang="ts">
const props = defineProps(['info'])
</script>

<template>
<div class="projects">

<h3>{{props.info.project}}</h3>
  <h3>{{props.info.year}}</h3>

  <p v-for="tech in props.info.technology"><-{{tech}}</p>



</div>
</template>

<style scoped>
.projects {
  border: solid #f30000 1px;
  min-width: 98%;
  min-height:55rem;
  border-radius:7px;
  padding: 0.5rem;


}
</style>