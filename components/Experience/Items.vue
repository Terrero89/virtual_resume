<script setup lang="ts">
const props = defineProps(['info'])
</script>


<template>
  <div class="education">

    <div class="education-wrapper wrap">

      <div class="item">


        <div class="header">
          <span>{{ info.dates }}</span>


        </div>

        <div class="info">
          <div class="title">
            <span>{{ info.position }} </span>  @
            <span>{{ info.company }}</span>
          </div>

          <p>{{ info.description }}</p>

          <span>{{ info.city }}</span>

        </div>


      </div>


    </div>


  </div>


</template>


<style scoped>
.title{

  margin-bottom: 1rem;
}
.wrap {
  box-shadow: 0px 5px 16px -7px rgb(107, 107, 107);
  -webkit-box-shadow: 0px 5px 16px -7px rgb(58, 58, 58);
  -moz-box-shadow: 0px 5px 16px -7px rgba(0, 0, 0, 1);
  width: 48rem;
  border: solid rgba(106, 106, 106, 0.10) 1px;

  border-radius: 5px;
  margin: 1rem auto;
  background-color: rgba(255, 255, 255, 0.09);

}

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

padding:0.5rem



}

.item .header {
 width: 100%;
margin-right: 1rem;
  margin-bottom: 1rem;




}

.item .info {




}

.item h1 {

  margin: 0.5rem auto;

  font-weight: bold;
  font-size: 1.1rem;
}

.item span {

color: #e4e4e4;

  font-weight: bold;
  font-size: 1rem;
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

display:flex;
justify-content: space-between;

  }
}


</style>