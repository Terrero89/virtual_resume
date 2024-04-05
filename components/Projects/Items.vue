<script setup lang="ts">
const props = defineProps(['info'])
</script>

<template>
<div class="projects">



  <p v-for="tech in props.info.technology"><-{{tech}}</p>



</div>
</template>

<style scoped>
.projects{

}
</style>