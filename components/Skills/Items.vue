<template>
  <section class="skills-wrapper">
    <div


    >

    </div>

    <div
        class="skill-box"

    >
      <div
          class="expertise-box"
          v-for="skills in skillsInfo"
          :key="skills.title"

      >
        <div class="expertise-text">
          <div class="expertise-title">
            <h3 v-if="skills.title === 'Front-end'">Front-end Tools</h3>

            <h3 v-else>Backend-end Tools</h3>
          </div>
          <p>
            {{ skills.text }}
          </p>
        </div>
        <div class="expertise-tech">
          <div class="technologies" v-if="skills.title === 'Front-end'">
            <ul v-for="tech in props.info.tech.frontend">
              <li>
                {{ tech }}
              </li>
            </ul>
          </div>

          <div class="technologies" v-if="skills.title === 'Backend'">
            <ul v-for="tech in props.info.tech.backend">
              <li>
                {{ tech }}
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>


const props = defineProps(['info'])

const skillsInfo = ref([
  {
    title: "Front-end",
    text: "I have solid experience using HMTL, CSS, And Javascript as well as UI Frameworks. I'm currently working with Vue Js ecosystem as my main stack, and progresively transitioning to React Js. ",
  },
  {
    title: "Backend",
    text: "Although not a Backend Developer, I have gained some familiarity with these tools. I have worked on projects where I have applied the fundamentals of each one of them. ",
  },
])

const frontend = ref([
  "Html",
  "Css",
  "Javascript",
  "Typescript",
  "React JS",
  "Vue Js",
  "Nuxt Js",
  "Bootstrap",
  "Tailwind",

])
const backend = ref([
  "Node Js",
  "Express Js",
  "Mongoose",
  "Firebase",
  "MongoDB",
  "Go"

])

</script>


<style scoped>


.expertise-box {
  margin: 1rem auto;
  border-radius: 10px;

  max-width: 55rem;

  border: solid rgba(106, 106, 106, 0.64) 1px;
  padding: 1rem;

  background-color: rgba(255, 255, 255, 0.09);
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
  margin: 0rem 2.5rem 0 0;
  font-size: 0.85rem;
  letter-spacing: 0.10rem;

  text-decoration: none;
  list-style: none;
  letter-spacing: 0.15rem;
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
  margin-top: 1rem;
}

.expertise-text p {

  margin: 1rem 0;
  font-size: 1rem;

}

.technologies {
  display: flex;
  flex-wrap: wrap;
  margin-right: 3rem;
}


</style>