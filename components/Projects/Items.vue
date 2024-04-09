<script setup lang="ts">
const props = defineProps(['info'])
</script>

<template>
  <div class="projects">

    <div class="projects-wrapper wrap" >

      <div class="item">


        <div class="header">
          <h1>{{ info.project}}</h1>
          <p>{{ info.description.slice(0, 100)}}... more</p>



        </div>
        <div  class="tech" v-for="tech in info.technology">
          <span class="tech-item">{{ tech}}</span>


        </div>

<!--        <p>{{ info.description.slice(0, 100)}}... more</p>-->






      </div>


    </div>


  </div>


</template>

<style scoped>
.tech{
  display: inline-block;
  align-content: center;
  ;
}

.tech-item{
  margin-right: 1rem;
  color: #61dbfb;
}
.wrap {
  box-shadow: 0px 5px 16px -7px rgb(107, 107, 107);
  -webkit-box-shadow: 0px 5px 16px -7px rgb(58, 58, 58);
  -moz-box-shadow: 0px 5px 16px -7px rgba(0,0,0,1);
  border: solid rgba(106, 106, 106, 0.10) 1px;
  padding: 0 1.5rem;
  border-radius: 10px;
  margin:1rem auto;
  background-color: rgba(255, 255, 255, 0.09);

}
.projects{
  border-radius: 7px;

}

.projects-wrapper {

  display: flex;
  flex-direction: row;
  align-items: center;
  align-content: center;

}

.education-wrapper .image {
  object-fit: cover;
}

.education img {
  object-fit: cover;
  height: 6rem;
  width: 6rem;
  border-radius: 7px;


}
.item {

  padding: 1rem;
  margin: auto  1rem;


}

.item .header{

  width: 12rem;




}
.item p{align-content: flex-end;




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

  font-weight: 400;
  font-size: 1rem;
  margin: 0.2rem auto;
}
@media only screen and (min-width: 470px) {
  .item {
    display: flex;
    justify-content: space-between;
    margin-right:  auto;



  }
}




</style>