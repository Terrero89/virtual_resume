<script setup>
const props = defineProps(["info"]);




</script>


<template>
  <section class="skills-wrapper">
 

    <div class="skill-box">
      <div
        class="expertise-box"
        v-for="skills in info"
        :key="skills.title"
      >
        <div class="expertise-text">
          <div class="expertise-title">
             <h3 v-if="skills.title === 'Front-end'">Front-end Tools</h3>
            <h3 v-else>Backend-end Tools</h3>
            
          </div>
          <p>

          </p>
        </div>
    
        <div class="expertise-tech">
          <div class="technologies" >
            <ul v-for="tech in skills.skills" :key="tech" >
              <li >
                {{ tech}}
              </li>
            </ul>
          </div>

       
        </div>
      </div>
    </div>
  </section>
</template>



<style scoped>
/* .expertise-box {
  margin: 0.5rem auto;
  border-radius: 10px;
  border: solid rgba(106, 106, 106, 0.64) 1px;
  padding: 1rem;
  background-color: rgba(255, 255, 255, 0.09);
   margin: 0.5rem ;
} */

/*.skill-box {
  margin: 1rem auto ;
  border-radius: 10px;
  border: solid rgba(106, 106, 106, 0.64) 1px;
  padding: 1rem;
  background-color: rgba(255, 255, 255, 0.09);
}
*/
.skill-box {
  margin: 2rem auto ;
  border-radius: 10px;
  border-bottom: solid rgba(106, 106, 106, 0.64) 1px;
  padding: 1rem;

}




.expertise-box h3 {
  font-weight: 700;
  text-decoration: none;
  list-style: none;

  font-size: 1.2rem;
}

.expertise-box ul li {
  text-decoration: none;
  list-style: none;

  font-size: 0.85rem;
  letter-spacing: 0.1rem;

  text-decoration: none;
  list-style: none;

}

.expertise-tech {
  display: flex;
  width: 100%;
  flex-wrap: wrap;
  margin: 1rem 0;
}

.expertise-tech .technologies ul li {
  font-family: "Inconsolata", monospace;
  color: #61dbfb;
  font-size: 0.85rem;
  margin-right: 1.3rem;
  margin-top: 0.3rem;
}

.expertise-text p {
  margin: 0.5rem 0;
  font-size: 1rem;
}

.technologies {
  display: flex;
  flex-wrap: wrap;
  margin-right: 3rem;
}

@media only screen and (max-width: 450px) {
  .expertise-box {
    width: 98%;
    margin: 0 auto;
    padding: 0;
  }
}
</style>
