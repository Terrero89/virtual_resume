<script setup lang="ts">
const props = defineProps(['info'])
</script>

<template>
<div class="skills">
  <div v-for="item in props.info.tech">{{item}}</div>




</div>
</template>

<style scoped>
.skills {
  border: solid #f30000 1px;
  min-width: 100%;
  min-height:55rem;
  border-radius:7px;
  padding: 0.5rem;


}
</style>