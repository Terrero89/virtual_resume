<script setup lang="ts">
const props = defineProps(['info'])
</script>

<template>
<div>
  <h3>{{props.info.header}}</h3>
  <h3>{{props.info.subtitle}}</h3>
  <h3>{{props.info.description}}</h3>



</div>
</template>

<style scoped>

</style>