<script setup lang="ts">
const props = defineProps(['info'])

let icons = ref("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='1em' height='1em' viewBox='0 0 256 256'%3E%3Cpath fill='white' d='M197.66 197.66a8 8 0 0 1-11.32 0L72 83.31V168a8 8 0 0 1-16 0V64a8 8 0 0 1 8-8h104a8 8 0 0 1 0 16H83.31l114.35 114.34a8 8 0 0 1 0 11.32'/%3E%3C/svg%3E")
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


          <h1>{{ info.position }} </h1> @
            <h3>{{ info.company }} </h3>

            <img :src="icons">



          </div>

          <p>{{ info.description }}</p>



        </div>


      </div>


    </div>


  </div>


</template>


<style scoped>
.title {
  display: inline;

  margin-bottom: 1rem;
}
.position-flex{
  display: flex;
}

.title img{
  min-height: 0.2rem;
  min-width: 0.3rem;

    transform: rotate(90deg);

  margin-left: 0.5rem;

  display: inline-block;
}

/*.wrap {
  box-shadow: 0px 5px 16px -7px rgb(107, 107, 107);
  -webkit-box-shadow: 0px 5px 16px -7px rgb(58, 58, 58);
  -moz-box-shadow: 0px 5px 16px -7px rgba(0, 0, 0, 1);
  width: 48rem;
  border: solid rgba(106, 106, 106, 0.10) 1px;

  border-radius: 5px;
  margin: 1rem auto;
  background-color: rgba(255, 255, 255, 0.09);

}*/
.wrap {

  width: 48rem;
  border-bottom: solid rgba(128, 128, 128, 0.41) 1px;

  border-radius: 5px;
  margin: 3rem auto;


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
  min-height: 1rem;
  width: 1.5rem;
  border-radius: 7px;


}

.item {

  padding: 0.5rem


}

.item .header {
  width: 100%;
  margin-right: 1rem;
  margin-bottom: 1rem;


}
.item .header div {
display: flex;
  justify-content: center;
  align-items: center;
}
.item .header img {
  margin: 0.4rem auto;
  height: 0.2rem;
}

.item .info {


}

.item h1 {
display: inline-block;


  font-weight: bold;
  font-size: 0.9em;
}
.item h3 {
  display: inline-block;
  font-weight: bold;
  font-size: 0.9em;
  margin: 0.2rem auto;
}

.item span {

  color: #e4e4e4;

  font-weight: bold;
  font-size: 1rem;
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
    justify-content: space-between;

  }
}


</style>