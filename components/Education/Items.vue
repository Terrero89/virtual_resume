<script setup lang="ts">
const props = defineProps(['info'])
</script>

<template>
<div>
  <h3> {{props.info.degree}}</h3>
  <h3>{{props.info.school}}</h3>
  <h3>{{props.info.year}}</h3>
  <h3>{{props.info.grad}}</h3>


</div>
</template>

<style scoped>

</style>