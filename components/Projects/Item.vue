
<script setup lang="ts">
const props = defineProps(['items'])


</script>

<template>
<div>
  <div class="tech" v-for="tech in items">
    <span class="tech-item">{{tech}}</span>
  </div>
</div>

</template>


<style scoped>
.tech {
  margin:1rem 0;
  max-width: 15rem;
  display: inline-block;
  flex-direction: column;


}

.tech .tech-item{

  padding: 0.5rem;
  border-radius: 12px;

  margin-right: 0.8rem;
  color:   #02d5fa;

  background-color: rgba(73, 152, 165, 0.25);
}

.tech .tech-item:hover{
  transform: scale(5);


  /*  color:   #02d5fa}*/
  color: #4998a5;
}

.tech-item :hover{
  transform: scale(1.5);
  color: #4998a5;
}
</style>