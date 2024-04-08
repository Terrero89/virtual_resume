<script setup lang="ts">
const props = defineProps(['info'])
</script>

<template>
  <div class="education">

    <div class="education-wrapper wrap">
      <div class="image">
        <img
            :src="props.info.schoolLogo"/>
      </div>
      <div class="item ">
        <h1>{{ props.info.school }}</h1>
        <h3>{{props.info.degreeType}} in {{ props.info.degree }}</h3>

        <p>{{ props.info.year }}</p>
        <h3>{{ props.info.grad  }}</h3>
      </div>

    </div>




  </div>
</template>

<style scoped>
.education {
  border-radius: 7px;

}

.education-wrapper{

  display: flex;
  flex-direction: row;
  align-items: center;
  align-content: center;

}

.education-wrapper .image{
  object-fit: cover;
}

.education img{
  object-fit: cover;
  max-height: 6rem;
  max-width: 8rem;
  border-radius: 7px;


}

.item{
  margin: 0.7em;
}
.item h1{

  margin: 0.5rem auto;

  font-weight: bold;
  font-size: 1.3rem;
}
.item h3{

  font-weight: bold;
  font-size: 1rem;
  margin: 0.2rem auto;
}
.item p{

  font-weight:400;
  font-size: 1rem;
  margin: 0.2rem auto;
}


.wrap {
  
  border: solid rgba(106, 106, 106, 0.64) 1px;
  padding: 0 1.5rem;
  border-radius: 10px;
  background-color: rgba(255, 255, 255, 0.09);

}
</style>