<script setup lang="ts">
const props = defineProps(['info'])
</script>

<template>
  <div class="education">

    <UIWrapper class="education-wrapper" v-for="item in props.info" :key="item.info">


      <div class="item">
        <div class="image">
          <img :src="item.schoolLogo" alt="school_logo"/>
        </div>
<div>



</div>
        <div class="info">
          <div class="title">
            <h1>{{ item.school }}</h1>
            <span>{{ item.degreeType }}</span>
            <span > in {{ item.degree }} </span>

          </div>
        </div>

        <div class="header">
          <span class="date">{{ item.dates }}</span>
        </div>
      </div>


    </UIWrapper>


  </div>


</template>

<style scoped>
.title {

  margin-bottom: 1rem;
}

/*.wrap { class="sub"
  box-shadow: 0px 5px 16px -7px rgb(107, 107, 107);
  -webkit-box-shadow: 0px 5px 16px -7px rgb(58, 58, 58);
  -moz-box-shadow: 0px 5px 16px -7px rgba(0, 0, 0, 1);
  width: 48rem;
  border: solid rgba(106, 106, 106, 0.10) 1px;
  padding: 0.3rem;
  border-radius: 5px;
  margin: 1rem auto;
  background-color: rgba(255, 255, 255, 0.09);

}*/



.education {
  border-radius: 7px;

}

.education-wrapper {
  width: 98%;
  display: flex;
flex-direction: column;


}

.education-wrapper .image {
  object-fit: cover;

width: 10rem;




}

.education img {
  object-fit: contain;
  height: 6rem;
  width: 6rem;
  border-radius: 7px;


}

.item {

  padding: 0.5rem


}

.item .header{

  margin-bottom: 1rem;

  width:10rem;


}

.item .info {

width:20rem;



}

.item h1 {

  margin: 0.5rem auto;

  font-weight: bold;
  font-size: 1.1rem;
}

.item span {

  color: #c8c8c8;

  font-weight: bold;
  font-size: 1rem;
}
.header .date {
  font-family: "Roboto", sans-serif;
  text-transform: uppercase;
  color: #b0b0b0;
  font-weight: bold;

  font-size: 0.75rem;
}



.item h3 {

  font-weight: bold;
  font-size: 0.9rem;
  margin: 0.2rem auto;
}

.item p {
  color: #cdcdcd;
  font-weight: 400;
  font-size: 1rem;
  margin: 0.2rem auto;
}

@media only screen and (min-width: 470px) {
  .item {

    display: flex;
    justify-content: space-evenly;


  }


}
@media only screen and (max-width: 470px) {
  .image{

margin: 1rem 0 ;


  }


}


.wrap:hover{
  background-color: rgba(148, 148, 148, 0.18);
  border: none;
  transition: 200ms linear;
}

</style>