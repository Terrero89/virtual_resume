
<script setup lang="ts">
import { ref } from "vue";
const props = defineProps(["contactInfo"]);




</script>

<template>
<div>

    <div class="">
        <h3>Contact</h3>
        <div class="contact">
          <div class="head">
            <img class="tab-icon" :src="contactInfo.email.icon" />
            <p>
              <NuxtLink
                to="mailto:recipient@example.com?subject=Hello&body=How are you?"
              >
                Sergio-terrero28@gmail.com
              </NuxtLink>
            </p>
          </div>
<!--          <div class="head">-->
<!--            <img class="tab-icon" :src="contactInfo.github.icon" />-->

<!--            <NuxtLink :to="contactInfo.github.value">-->
<!--              {{ contactInfo.github.value }}</NuxtLink-->
<!--            >-->
<!--          </div>-->

          <div class="head">
            <img class="tab-icon" :src="contactInfo.portfolio.icon" />
            <NuxtLink :to="contactInfo.email.value"> {{ contactInfo.email.value }}</NuxtLink>
          </div>
<!--          <div class="head">-->
<!--            <img class="tab-icon" :src="contactInfo.linkedin.icon" />-->
<!--            <NuxtLink :to="contactInfo.linkedin.value">-->
<!--              {{ contactInfo.linkedin.value.slice(0, 42) }}</NuxtLink-->
<!--            >-->
<!--          </div>-->
        </div>
      </div>
</div>

</template>


<style scoped>



.contact {
  padding: 0.5rem;
  display: flex;

  flex-wrap: wrap;
}

.contact p {
  font-size: 1.5rem;
}

.head {
  margin: 0.5rem 0;
  display: flex;

}
.head img {
  align-content: center;
  align-items: center;
}

.wrap .contact a {
  margin-right: 1em;
  font-size: 0.85rem;
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

.about-item p a {
  font-size: 0.5rem;
}



</style>