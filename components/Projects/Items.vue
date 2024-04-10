<script setup lang="ts">
const props = defineProps(['info'])


const isModalOpen = ref(false);

const openModal = () => {
  isModalOpen.value = true;
};

const closeModal = () => {
  isModalOpen.value = false;
};
</script>




<template>
  <div class="education">

    <div class="education-wrapper wrap" >

      <div class="item">
        <div class="header">
          <h1>{{ info.project }}</h1>
          <h3>{{ info.description.slice(0,12)}}</h3>


        </div>

        <div class="info">
          <div class="tech" v-for="tech in info.technology">
            <span class="tech-item">{{tech}}</span>
          </div>


        </div>



      </div>


    </div>


  </div>


</template>
<style scoped>
.tech{
  max-width:15rem;
  display: inline-block;
  flex-direction: column;


}

.tech .tech-item{
margin-right: 0.8rem;

  color: #61dbfb;

}
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
  object-fit:cover;
  min-height: 6rem;
  width: 6rem;
  border-radius: 7px;


}

.item {

  padding: 0.8rem 1rem;




}

.item .header{
  width: 12rem;

  margin-right: 1rem;



}
.item .info{
  margin:0 auto ;
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