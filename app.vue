<script setup lang="ts">
import { ref } from "vue";

const props = defineProps(["info"]);

const tabs = ref([
  {
    label: "About",
    icon: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='1.2em' height='1.2em' viewBox='0 0 24 24'%3E%3Cpath fill='white' d='M9.833 11.385q-.472 0-.786-.348q-.314-.349-.247-.825l.306-2.393q.142-1.06.973-1.747q.83-.687 1.921-.687t1.921.687q.83.688.973 1.747l.306 2.393q.067.476-.247.825q-.314.348-.786.348zm-.058-1h4.45l-.325-2.4q-.1-.7-.637-1.15T12 6.385q-.725 0-1.262.45t-.638 1.15zM5 18.615V16.97q0-.619.36-1.158q.361-.54.97-.838q1.416-.679 2.833-1.018q1.418-.34 2.837-.34q1.42 0 2.837.34q1.417.34 2.832 1.018q.61.298.97.838q.361.539.361 1.158v1.646zm1-1h12v-.646q0-.332-.214-.625q-.215-.292-.594-.494q-1.234-.598-2.546-.916q-1.31-.319-2.646-.319q-1.335 0-2.646.319q-1.312.318-2.546.916q-.38.202-.594.494Q6 16.637 6 16.97zm6 0'/%3E%3C/svg%3E",
    content: [
      {
        header: "About me",
        sub: "Part of my story",
        text: "I am a dynamic and results-oriented individual with 5+ years of experience in the healthcare industry transitioning to software development. Passionate about technology with a focus on delivering creative quantitative solutions. Seeking a role where I can learn and grow in the industry while adding value to a dynamic team.",
        techStack: [
          "Html",
          "Css",
          "Javascript",
          "Typescript",
          "React JS",
          "Vue Js",
          "Nuxt Js",
          "Bootstrap",
          "Tailwind",
          "Node Js",
          "Express Js",
          "Mongoose",
          "Firebase",
          "MongoDB",
          "Go",
        ],
      },
    ],
  },
  {
    label: "Education",
    icon: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='1.2em' height='1.2em' viewBox='0 0 16 16'%3E%3Cpath fill='white' fill-rule='evenodd' d='M6.836 3.202L1.74 5.386a.396.396 0 0 0 0 .728l5.096 2.184a2.5 2.5 0 0 0 .985.202h.358a2.5 2.5 0 0 0 .985-.202l5.096-2.184a.396.396 0 0 0 0-.728L9.164 3.202A2.5 2.5 0 0 0 8.179 3h-.358a2.5 2.5 0 0 0-.985.202M1.5 7.642l1.5.644v3.228a2 2 0 0 0 1.106 1.789l.806.403a7 7 0 0 0 6.193.033l.909-.442a2 2 0 0 0 1.125-1.798V8.226l1.712-.734a1.896 1.896 0 0 0 0-3.484L9.755 1.823A4 4 0 0 0 8.179 1.5h-.358a4 4 0 0 0-1.576.323L1.15 4.008A1.896 1.896 0 0 0 0 5.75v4.5a.75.75 0 0 0 1.5 0zm3 3.872V8.929l1.745.748A4 4 0 0 0 7.821 10h.358a4 4 0 0 0 1.576-.323l1.884-.808v2.63a.5.5 0 0 1-.282.45l-.909.442a5.5 5.5 0 0 1-4.865-.027l-.807-.403a.5.5 0 0 1-.276-.447' clip-rule='evenodd'/%3E%3C/svg%3E",
    content: [
      {
        degree: "Information Technology",
        degreeType: "Bachelors",
        school: "University Of Massachusetts Boston ",
        schoolLogo:
          "https://upload.wikimedia.org/wikipedia/commons/thumb/c/c7/UMass-Lowell_logo.svg/1200px-UMass-Lowell_logo.svg.png",
        dates: "2020 - 2023",
        grad: true,
      },
      {
        degree: "Computer Science",
        degreeType: "Associates",
        school: "Quincy Community College",
        schoolLogo:
          "https://www.excelsior.edu/wp-content/uploads/2018/01/logo-quincy-300x210.jpeg",
        dates: "2018 - 2020",
        grad: true,
      },
      {
        degree: "Cloud Practitioner Certificate",
        school: "AWS",
        schoolLogo:
          "https://lab651.com/wp-content/uploads/2023/07/Amazon-Web-Services-AWS-Logo.png",
        degreeType: "Certificate",
        dates: "In Progress",
        grad: false,
      },
    ],
  },
  {
    label: "Experience",
    icon: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='1.2em' height='1.2em' viewBox='0 0 512 512'%3E%3Cpath fill='white' d='M375.344 18.438c-1.137-.01-2.276.007-3.438.03c-13.273.27-28.187 2.787-45.562 8.126c-22.4 6.883-38.08 27.877-35.844 50.312c1.62 16.34 15.186 34.143 30.875 45.625c24.664 18.046 42.29 36.65 54.375 54.44l7.625 48.843l18.47-2.907l-5.064-32.437c-1.34-23-7.98-45.714-22.342-69.095c14.54 8.79 27.36 18.46 38.03 28.156l28.22 55.72l16.656-8.438l-26.53-52.406c-7.148-17.347-17.845-33.647-33.783-49.03c15.97 4.774 30.48 10.84 42.97 17.436l39.906 45.22l14-12.376l-40.5-45.875l-.094.095C441.37 85.048 426.1 72.19 406.063 61.687v-.093c-.278-.243-.558.187-.812.187c-25.3-1.83-47.73-.167-62.28 3.69c13.373-10.633 34.805-18.547 64.592-21.25l47.375 18.31l6.75-17.436l-41.375-16l-.093-.032c-13.467-6.492-27.824-10.464-44.876-10.625m-237.688.03c-16.838.232-31.037 4.164-44.375 10.595l-41.468 16.03l6.72 17.438l47.406-18.31c29.77 2.706 51.224 10.62 64.593 21.25c-14.55-3.857-36.98-5.52-62.28-3.69c-.254 0-.534-.43-.813-.186v.093C87.4 72.192 72.132 85.047 60.188 99.876l-.124-.094l-40.5 45.876l14.03 12.375l39.906-45.22c12.49-6.596 27-12.662 42.97-17.437c-15.94 15.384-26.668 31.684-33.814 49.03l-26.53 52.407l16.687 8.438L101 149.53c10.672-9.694 23.49-19.366 38.03-28.155c-14.36 23.38-21 46.095-22.343 69.094l-5.03 32.436l18.468 2.906l7.594-48.78c12.084-17.806 29.684-36.437 54.374-54.5c15.69-11.483 29.254-29.286 30.875-45.626c2.234-22.435-13.414-43.43-35.814-50.312c-19.113-5.873-35.252-8.32-49.5-8.125zM307.72 235.814c-11.41 0-24.272 4.91-40.22 22.718v130.814c19.24-13.898 38.485-19.628 56.563-19.844c22.987-.275 43.643 7.632 61.562 15.438c17.92 7.805 33.542 15.33 44.156 16.468c5.308.57 9.002-.088 12.564-2.312c3.187-1.99 6.62-5.816 10-12.53L431.688 256.81c-10.648 7.425-20.88 11.553-30.72 12.688c-13.806 1.592-26.063-2.53-36.75-7.97c-21.37-10.875-38.164-25.762-56.5-25.717zm-99.376 5c-18.118-.082-35.583 15.45-57.406 27.093c-10.912 5.822-23.348 10.394-37.407 9.156c-10.018-.88-20.423-4.782-31.186-12.156L62.906 393.47c13.616 13.096 25.344 15.566 38.594 13.842c14.267-1.855 30.332-9.854 47.406-18.093c17.074-8.24 35.31-16.776 55.438-17.22c14.575-.32 29.73 4.21 44.47 15.344V259.47c-16.255-18.45-24.774-18.62-40.47-18.658zM45.438 278.875l-24.782 158.22l194.906 13v19h83.563v-18.97l195.53-13.03l-24.78-158.22l-15.53 1.22l16.936 106.5l.44 2.78l-1.158 2.53c-4.76 10.555-10.745 18.306-18.312 23.033c-3.66 2.285-7.59 3.727-11.594 4.53l.03.188l-1.998.188c-.084.012-.167.02-.25.03c-.958.136-1.915.217-2.875.282h-.125L258.563 437.28l-.782.064l-.75-.063l-158.467-10.967h-.094c-4.606.203-9.278-.1-13.97-.97c-.03-.005-.063.006-.094 0c-13.02-2.434-26.164-9.29-38.25-22.124l-3.125-3.314l.69-4.5l17.405-115.312l-15.688-1.22zM324.28 388.188c-18.502.22-37.827 6.678-59.436 27.625l-2.344 2.28l124.563-12.03c-2.944-1.34-5.893-2.688-8.907-4c-17.257-7.518-35.372-14.096-53.875-13.875zm-119.53 2.5c-14.906.328-30.94 7.28-47.72 15.375c-3.318 1.6-6.69 3.246-10.06 4.875L254 418.344l-2.72-3.125c-17.09-19.683-31.624-24.86-46.53-24.533z'/%3E%3C/svg%3E",
    content: [
      {
        company: "Liberty Mutual Insurance",
        city: "Boston, MA",
        position: "Software Engineer",
        dates: "2024 -- present",
        technologies: [
          "React",
          "Node Js",
          "Express",
          "MongoDB, AWS, Typescript",
        ],
        description:
          "One of the more than 120 people selected into 2023 Hack.Diversity Fellowship, a career leadership and workforce\n" +
          "development program integrating Boston’s innovation, corporate, civic, academic, and philanthropic pillars.",
      },
      {
        company: "Hack Diversity",
        city: "Boston, MA",
        position: "Software Engineer Fellow",
        dates: "2024 -- present",
        technologies: ["React", "Node Js", "Express", "MongoDB"],
        description:
          "One of the more than 120 people selected into 2023 Hack.Diversity Fellowship, a career leadership and workforce\n" +
          "development program integrating Boston’s innovation, corporate, civic, academic, and philanthropic pillars.",
      },

      {
        company: "BCBSMA",
        city: "Hingham, MA",
        position: "Enrollment Processor III",
        dates: "2022 -- Present",
        technologies: [],
        description:
          "One of the more than 120 people selected into 2023 Hack.Diversity Fellowship, a career leadership and workforce\n" +
          "development program integrating Boston’s innovation, corporate, civic, academic, and philanthropic pillars.",
      },
      {
        company: "BCBSMA",
        city: "Hingham, MA",
        position: "Data Analyst (Job Shadow)",
        dates: "2022 -- 2022",
        technologies: ["Python", "Access", "Excel"],
        description:
          "One of the more than 120 people selected into 2023 Hack.Diversity Fellowship, a career leadership and workforce\n" +
          "development program integrating Boston’s innovation, corporate, civic, academic, and philanthropic pillars.",
      },
      {
        company: "BCBSMA",
        city: "Hingham, MA",
        position: "Directory & Audit Processor",
        dates: "2018 -- 2022",
        technologies: [],
        description:
          "One of the more than 120 people selected into 2023 Hack.Diversity Fellowship, a career leadership and workforce\n" +
          "development program integrating Boston’s innovation, corporate, civic, academic, and philanthropic pillars.",
      },
    ],
  },
  {
    label: "Projects",
    icon: "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='1.2em' height='1.2em' viewBox='0 0 32 32'%3E%3Cg fill='white'%3E%3Cpath d='M17 18v-2h-2v2H3v6h2v-4h10v4h2v-4h10v4h2v-6z'/%3E%3Cpath d='M4 32a3 3 0 1 1 0-6a3 3 0 0 1 0 6m0-4a1 1 0 1 0 0 2a1 1 0 0 0 0-2m12 4a3 3 0 1 1 0-6a3 3 0 0 1 0 6m0-4a1 1 0 1 0 0 2a1 1 0 0 0 0-2m12 4a3 3 0 1 1 0-6a3 3 0 0 1 0 6m0-4a1 1 0 1 0 0 2a1 1 0 0 0 0-2M23 8V6h-2.1a5 5 0 0 0-.73-1.75l1.49-1.49l-1.42-1.42l-1.49 1.49A5 5 0 0 0 17 2.1V0h-2v2.1a5 5 0 0 0-1.75.73l-1.49-1.49l-1.42 1.42l1.49 1.49A5 5 0 0 0 11.1 6H9v2h2.1a5 5 0 0 0 .73 1.75l-1.49 1.49l1.41 1.41l1.49-1.49a5 5 0 0 0 1.76.74V14h2v-2.1a5 5 0 0 0 1.75-.73l1.49 1.49l1.41-1.41l-1.48-1.5A5 5 0 0 0 20.9 8zm-7 2a3 3 0 1 1 0-6a3 3 0 0 1 0 6' class='ouiIcon__fillSecondary'/%3E%3Cpath d='M16 8a1 1 0 0 1-1-1a1.39 1.39 0 0 1 0-.2a.65.65 0 0 1 .06-.18a.74.74 0 0 1 .09-.18a1.61 1.61 0 0 1 .12-.15a.93.93 0 0 1 .33-.21a1 1 0 0 1 1.09.21l.12.15a.78.78 0 0 1 .09.18a.62.62 0 0 1 .1.18a1.27 1.27 0 0 1 0 .2a1 1 0 0 1-1 1'/%3E%3C/g%3E%3C/svg%3E",
    content: [
      {
        project: "Xray App",
        type: "Project",
        year: "2024",
        description:
          "(CRUD) application using the MERN stack for radiology reports as an assessment of x-ray images for exams of patients with COVID-19",
        link: "LINK",
        technology: ["React", "Express", "Node", "MongoDB"],
        image:
          "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.crazyegg.com%2Fblog%2Fhow-to-host-a-website%2F&psig=AOvVaw0dl_uYk8w64ZXV5T4j_flG&ust=1712794477616000&source=images&cd=vfe&opi=89978449&ved=0CBIQjRxqFwoTCPDm3OSutoUDFQAAAAAdAAAAABAE",
      },
      {
        project: "Foodie App",
        type: "Personal Project",
        year: "2023",
        description:
          "Simple React.Js practice application UI that displays information entered for finance tracking purposes. At this time application displays entered information, filter by month and year as a way to show features of the application.",
        link: "https://foodieapp2023.netlify.app/",
        technology: ["Node", "React", "Express", "Mongoose", "MongoDB"],
        image:
          "https://upload.wikimedia.org/wikipedia/commons/thumb/c/c7/UMass-Lowell_logo.svg/1200px-UMass-Lowell_logo.svg.png",
      },
      {
        project: "Find a Mentor",
        type: "Personal Project",
        year: "2021",
        description:
          "Web application built using Vue js ecosystem. This application allows to sign up, display information about types of services offered and allow users to send messages to the mentor listed in our system for hiring.",

        link: "https://find-mentor-project.web.app",
        technology: ["VueJs", "Firebase", "Vuex", "Vue Router", "JWT"],
        image:
          "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.crazyegg.com%2Fblog%2Fhow-to-host-a-website%2F&psig=AOvVaw0dl_uYk8w64ZXV5T4j_flG&ust=1712794477616000&source=images&cd=vfe&opi=89978449&ved=0CBIQjRxqFwoTCPDm3OSutoUDFQAAAAAdAAAAABAE",
      },
      {
        project: "My Web blog",
        type: "Personal Project",
        year: "2021",
        description:
          "Personal Blog where I intend to post different articles and posts about technology, and other topics. This web app also allows users to sign up, sign in, as well as post articles and blogs of their preference. The ideas was to allow users to interact with others user through the blog as well.",
        link: "https://sergioterreroblog.netlify.app/",
        technology: ["Nuxt js", "Vuex", "JWT", "Firebase", "Axios"],
        image:
          "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.crazyegg.com%2Fblog%2Fhow-to-host-a-website%2F&psig=AOvVaw0dl_uYk8w64ZXV5T4j_flG&ust=1712794477616000&source=images&cd=vfe&opi=89978449&ved=0CBIQjRxqFwoTCPDm3OSutoUDFQAAAAAdAAAAABAE",
      },
      {
        project: "Finance Tracker UI",
        type: "Personal Project",
        year: "2023",
        description:
          "Simple React.Js practice application UI that displays information entered for finance tracking purposes. At this time application displays entered information, filter by month and year as a way to show features of the application.",
        link: "https://financetracker2023.netlify.app/",
        technology: ["Node", "React", "Express", "Mongoose", "MongoDB"],
        image:
          "https://upload.wikimedia.org/wikipedia/commons/thumb/c/c7/UMass-Lowell_logo.svg/1200px-UMass-Lowell_logo.svg.png",
      },
    ],
  },
]);
</script>

<template>
  <div>
    <UContainer class="main-container">
      <div class="main-wrapper">
        <UIHeader />
        <UITabs :tabList="tabs" />
      </div>
    </UContainer>
  </div>
</template>

<style scoped>
.co {
  width: 100%;
}

.main-wrapper {
  margin: 0.5rem auto;
  border-radius: 12px;
  min-height: 90vh;
  background: rgb(0, 0, 0);
  background: linear-gradient(
    175deg,
    rgb(6, 21, 43) 0%,
    rgb(26, 36, 44) 46%,
    rgb(23, 89, 119) 95%
  );
  border: solid #4f4f4f 1px;
  background-position: center;
  background-origin: content-box;
  background-repeat: no-repeat;
  background-clip: content-box;
}

@media only screen and (min-width: 1080px) {
  .main-container {
    min-width: 47%;
  }
}

@media only screen and (max-width: 450px) {
  .main-container {
    padding: 0;
  }

  .main-wrapper {
    margin: 0 auto;
    border-radius: 0;
  }
}
</style>
