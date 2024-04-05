<script setup lang="ts">
const props = defineProps(['info'])
</script>

<template>
<div class="about-item">

  <h3>{{props.info.header}}</h3>
  <h5 class="sub">{{props.info.sub}}</h5>
  <p>{{props.info.text}}</p>



</div>
</template>

<style scoped>
.about-item {

  max-width: 35rem;

}
.about-item h3{
margin: 0.5rem 0;
  font-weight: 700;
  font-size: 2.5rem;
}
.about-item .sub{
margin-bottom: 0.5rem;
  font-size: 1.5rem;
  font-weight: 600;
}

.about-item p{
  margin-bottom: 0.5rem;
  font-size: 0.85rem;
}
</style>