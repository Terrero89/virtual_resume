<script setup lang="ts">
const props = defineProps(['info'])
</script>

<template>
<div>
  <div v-for="item in props.info.tech">{{item}}</div>




</div>
</template>

<style scoped>

</style>