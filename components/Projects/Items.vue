<script setup lang="ts">
const props = defineProps(['info'])


</script>


<template>
  <div class="education">



    <UIWrapper class="education-wrapper">

      <div class="item">
        <div class="header">
          <h1>{{ info.project }}</h1>
          <p>{{ info.description}}</p>


        </div>

        <div class="info">

          <ProjectsItem :items="info.technology"/>

        </div>


      </div>


    </UIWrapper>


  </div>


</template>
<style scoped>





.education {
  border-radius: 7px;

}

.education-wrapper {
  width: 98%;
  display: flex;
  flex-direction: row;
  align-items: center;
  align-content: center;


}

.education-wrapper .image {
  object-fit: contain;

}

.education img {
  object-fit: cover;
  min-height: 6rem;
  width: 6rem;
  border-radius: 7px;


}

.item {

  padding: 0.8rem 0.8rem;


}

.item .header {
  width: 24rem;

  margin-right: 1rem;


}

.item .info {

  margin: 0 auto;
  align-content: flex-end;
  align-items: flex-end;


}

.item h1 {

  margin: 0.5rem auto;

  font-weight: bold;
  font-size: 1.1rem;
}

.item h3 {

  font-weight: bold;
  font-size: 0.9rem;
  margin: 0.2rem auto;
}

.item p {
color: #cacaca;
  font-weight: 400;
  font-size: 1rem;
  margin: 0.2rem auto;
}

@media only screen and (min-width: 470px) {
  .item {
    display: flex;
    justify-content: space-between;
    margin-right: auto;


  }
}

.wrap:hover{
  background-color: rgba(148, 148, 148, 0.18);
  border: none;
  transition: 200ms linear ;
  color: #02d5fa;
}

</style>