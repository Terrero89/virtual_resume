<script setup lang="ts">
const props = defineProps(['info'])

let icons = ref("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='1em' height='1em' viewBox='0 0 256 256'%3E%3Cpath fill='white' d='M197.66 197.66a8 8 0 0 1-11.32 0L72 83.31V168a8 8 0 0 1-16 0V64a8 8 0 0 1 8-8h104a8 8 0 0 1 0 16H83.31l114.35 114.34a8 8 0 0 1 0 11.32'/%3E%3C/svg%3E")
</script>


<template>
  <div class="education">

    <UIWrapper class="education-wrapper">

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


    </UIWrapper>


  </div>


</template>


<style scoped>
.title {
  display: inline;

  margin-bottom: 1rem;
}

.position-flex {
  display: flex;
}

.title img {
  min-height: 0.2rem;
  min-width: 0.3rem;

  transform: rotate(90deg);

  margin-left: 0.5rem;

  display: inline-block;
}




.education {
  border-radius: 7px;

}

.education-wrapper {

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
  font-size: 1rem;
}

.item h3 {
  display: inline-block;
  font-weight: bold;
  font-size: 1rem;
  margin: 0.2rem auto;
  color: #02d5fa;
}

.item span {
  font-family: "Roboto", sans-serif;
  text-transform: uppercase;
  color: #b0b0b0;
  font-weight: bold;

  font-size: 0.75rem;
}


.item p {
  color: #cdcdcd;
  font-weight: 400;
  font-size: 1rem;
  margin: 0.3rem auto;

}

@media only screen and (min-width: 470px) {
  .item {

    display: flex;
    justify-content: space-between;

  }
}


.wrap:hover {
  background-color: rgba(148, 148, 148, 0.18);
  border: none;
  transition: 200ms linear;
}

/* .wrap:hover {
  background-image: url("https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSH9YDoanr87yZhzZjoOUHN1puoZls7s32cfw&s");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  opacity:0.1;
}  */
</style>