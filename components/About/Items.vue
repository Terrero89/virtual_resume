<script setup lang="ts">
const props = defineProps(['info'])

let info = ref({
  email:{value:"https://sergioterrero.netlify.app" , icon: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='1rem' height='1rem' viewBox='0 0 24 24" +
      "'%3E%3Cpath fill='%23f7f7f7' d='M21 2H6a2 2 0 0 0-2 2v3H2v2h2v2H2v2h2v2H2v2h2v3a2 2 0 0 0 2 2h15a1 1 0 0 0 1-1V3a1 " +
      "1 0 0 0-1-1m-8 2.999c1.648 0 3 1.351 3 3A3.012 3.012 0 0 1 13 11c-1.647 0-3-1.353-3-3.001c0-1.649 1.353-3 3-3M19 18H7v-." +
      "75c0-2.219 2.705-4.5 6-4.5s6 2.281 6 4.5z'/%3E%3C/svg%3E"},
  github: {value: 'https://github.com/Terrero89', icon: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='1rem' height='1rem' viewBox='0 0 24 24'%3E%3Cpath " +
      "fill='%23f5ebeb' d='M12 .297c-6.63 0-12 5.373-12 12c0 5.303 3.438 9.8 8.205 11.385c.6.113.82-.258.82-.577c0-.285-.01-1.04-." +
      "015-2.04c-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729c1.205.084 1.838" +
      " 1.236 1.838 1.236c1.07 1.835 2.809 1.305 3.495.998c.108-.776.417-1.305.76-1.605c-2.665-.3-5.466-1.332-5.466-5.93c0-1.31." +
      "465-2.38 1.235-3.22c-.135-.303-.54-1.523.105-3.176c0 0 1.005-.322 3.3 1.23c.96-.267 1.98-.399 3-.405c1.02.006 2.04.138 3 " +
      ".405c2.28-1.552 3.285-1.23 3.285-1.23c.645 1.653.24 2.873.12 3.176c.765.84 1.23 1.91 1.23 3.22c0 4.61-2.805 5.625-5.475" +
      " 5.92c.42.36.81 1.096.81 2.22c0 1.606-.015 2.896-.015 3.286c0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627" +
      "-5.373-12-12-12'/%3E%3C/svg%3E"},

  portfolio:{value: "https://sergioterrero.netlify.app", icon: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='1rem' height='1rem' viewBox='0 0 20" +
      " 20'%3E%3Cpath fill='%23f5ebeb' d='M4 5H.78c-.37 0-.74.32-.69.84l1.56 9.99S3.5 8.47 3.86 6.7c.11-.53.61-.7.98-.7H10s-." +
      "7-2.08-.77-2.31C9.11 3.25 8.89 3 8.45 3H5.14c-.36 0-.7.23-.8.64C4.25 4.04 4 5 4 5m4.88 0h-4s.42-1 .87-1h2.13c.48 0 1 1 1" +
      " 1M2.67 16.25c-.31.47-.76.75-1.26.75h15.73c.54 0 .92-.31 1.03-.83c.44-2.19 1.68-8.44 1.68-8.44c.07-.5-.3-.73-.62-.73H16V5" +
      ".53c0-.16-.26-.53-.66-.53h-3.76c-.52 0-.87.58-.87.58L10 7H5.59c-.32 0-.63.19-.69.5c0 " +
      "0-1.59 6.7-1.72 7.33c-.07.37-.22.99-.51 1.42M15.38 7H11s.58-1 1.13-1h2.29c.71 0 .96 1 .96 1'/%3E%3C/svg%3E"},

linkedin: {value: "https://www.linkedin.com/in/sergio-terrero-34045a11b", icon: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='1rem' height='1rem' " +
      "viewBox='0 0 16 16'%3E%3Cpath fill='%23f5ebeb' d='M0 1.146C0 .513.526 0 1.175 0h13.65C15.474 0 16 .513 16 1.146v13.708c0 .633-.526 1.146-1.175 1" +
      ".146H1.175C.526 16 0 15.487 0 14.854zm4.943 12.248V6.169H2.542v7.225zm-1.2-8.212c.837 0 1.358-.554 1.358-1.248c-.015-.709-.52-1.248-1.342-1.248S2.4 " +
      "3.226 2.4 3.934c0 .694.521 1.248 1.327 1.248zm4.908 8.212V9.359c0-.216.016-.432.08-.586c.173-.431.568-.878 1.232-.878c.869 0 1.216.662 1.216 1.634v3." +
      "865h2.401V9.25c0-2.22-1.184-3.252-2.764-3.252c-1.274 0-1.845.7-2.165 1.193v.025h-.016l.016-.025V6.169h-2.4c.03.678 0 7.225 0 7.225z'/%3E%3C/svg%3E"},
})


</script>

<template>
  <div class="about-item">

    <div class="about-wrapper">
      <div class="bio wrap">
        <h3>About me</h3>
        <p>{{ props.info.text }}</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam vestibulum ac ante sit amet porta. Ut
           </p>
      </div>
      <div class="bio wrap">
        <h3>Bio</h3>
        <p>{{ props.info.text }}</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam vestibulum ac ante sit amet porta. Ut
          faucibus ante vehicula odio tempus, mollis aliquam neque porttitor. Donec eu tellus ex. Donec rhoncus neque
          vitae nisi fermentum, sit amet mattis elit venenatis. Suspendisse hendrerit suscipit turpis. Phasellus non
          tr</p>
      </div>


      <div class="wrap">
        <h3>Contact</h3>
        <div class="contact">
          <div class="head">
            <img class="tab-icon" :src="info.email.icon">
            <p> <NuxtLink to="mailto:recipient@example.com?subject=Hello&body=How are you?"> Sergio-terrero28@gmail.com </NuxtLink> </p>
          </div>
          <div class="head">
            <img class="tab-icon" :src="info.github.icon">

            <NuxtLink :to="info.github.value"> {{info.github.value}}</NuxtLink>
          </div>


          <div class="head">
            <img class="tab-icon" :src="info.portfolio.icon">
            <NuxtLink :to="info.email.value"> {{info.email.value}}</NuxtLink>
          </div>
          <div class="head">
            <img class="tab-icon" :src="info.linkedin.icon">
            <NuxtLink :to="info.linkedin.value"> {{info.linkedin.value.slice(0,42)}}</NuxtLink>
          </div>




        </div>
      </div>


    </div>


  </div>
</template>

<style scoped>
.about-item {
  width: 98%;
  border-radius: 7px;
  padding: 0.5rem;
  display: flex;
  justify-content: center;
}

.about-wrapper {
  margin: 0.5rem 0;
  display: flex;
  justify-content: center;

  flex-direction: column;
  max-width: 50rem;
}

.bio{

}
.contact {
  padding: 0.5rem ;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;

}

.contact p {
  font-size: 1.5rem;

}



.head{
margin: 0.5rem 0;
display: flex;
justify-content: space-around;




}
.head img{


  align-content: center;
  align-items: center;



}

.wrap .contact a{
  font-size: 0.85rem;

}

.wrap {


  border: solid rgba(106, 106, 106, 0.64) 1px;
  padding: 0.8rem;
  border-radius: 7px;
  margin: 0.5rem 0;
  background-color: rgba(255, 255, 255, 0.09);

}

.tab-icon {
align-content: center;
  align-items: center;
  height: 1.8rem;

  margin-right: 0.5rem;

}


.about-item h3 {
  font-family: "Montserrat", sans-serif;
  display: inline-block;
  margin: 0.5rem 0;
  font-weight: 700;
  font-size: 1.1rem;
}

.about-item .sub {
  margin-bottom: 0.5rem;
  font-size: 1.2rem;
  font-weight: 600;
}

.about-item p {
  margin-bottom: 0.5rem;
  font-size: 0.85rem;
}

.about-item  p a{

  font-size: 0.5rem;
}
</style>