<script setup lang="ts">
const props = defineProps(['info'])
</script>

<template>
  <div class="education">

    <div class="education-wrapper wrap" v-for="item in props.info" :key="item.info">
      <div class="image">
        <img :src="item.schoolLogo"/>
      </div>
      <div class="item">
        <div class="header">
          <h3>{{ item.degreeType }}</h3>
          <h1>{{ item.degree }}</h1>

        </div>

        <div class="info">
          <h1>{{ item.school }}</h1>
          <span>{{ item.dates }}</span>


        </div>



      </div>


    </div>


  </div>


</template>

<style scoped>

.wrap {
  box-shadow: 0px 5px 16px -7px rgb(107, 107, 107);
  -webkit-box-shadow: 0px 5px 16px -7px rgb(58, 58, 58);
  -moz-box-shadow: 0px 5px 16px -7px rgba(0,0,0,1);
width: 48rem;
  border: solid rgba(106, 106, 106, 0.10) 1px;
  padding: 0 1.5rem;
  border-radius: 10px;
  margin:1rem auto;
  background-color: rgba(255, 255, 255, 0.09);

}
.education {
  border-radius: 7px;

}

.education-wrapper {
width: 96%;
  display: flex;
  flex-direction: row;
  align-items: center;
  align-content: center;


}

.education-wrapper .image {
  object-fit: contain;
  height: 6rem;
  width: 6rem;

}

.education img {
  object-fit:contain;
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
.item .info{
margin-right:  auto;




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