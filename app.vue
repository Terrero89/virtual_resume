<script setup lang="ts">
const items = [
  {
    key: "About me",
    label: "About",
    subtitle:'The good',
    description:
      "Information About me etc...Information about education etc.." +
      "Information about education etc..Information about education etc..Information About me etc...Information about education etc.." +
      "Information about education etc..Information about education etc..Information About me etc...Information about education etc.." +
      "Information about education etc..Information about education etc.. \n\n ffdfd",
  },
  {
    key: "Education",
    label: "Education",
    subtitle:'The good',
    description: "Information about education etc..",
  },
  {
    label: "Skills",
    key: "Technologies",
    subtitle:'The good',
    description: "Skills highlighted by used etc.. ",
    tech: ["Go", "Java", "Pearl", "Javascript", "React", "Vue"],
  },
  {
    label: "Experience",
    subtitle:'The good',
    key: "What I know",
    description: "And, this is the content for Tab2",
  },
];
</script>

<template>
  <div>
    <UContainer class="co">
      <div class="main-wrapper">

<UIHeader/>
<UITabs/>

      </div>
    </UContainer>
  </div>
</template>

<style scoped>

.co{
min-width: 100%;
}
@media only screen and (min-width:1080px){
.co{
  min-width: 60%;
}
}
@media only screen and (max-width:450px){
  .co{
padding: 0;
  }
}


.main-wrapper {

min-height: 90vh;
  background: rgb(0, 0, 0);
  background: linear-gradient(175deg, rgb(6, 21, 43) 0%, rgb(26, 36, 44) 46%, rgb(23, 89, 119) 95%);
  /*background: rgb(17,17,120);
  background: linear-gradient(90deg, rgba(17,17,120,1) 0%, rgba(6,148,189,1) 85%, rgba(0,212,255,1) 100%, rgba(2,0,36,1) 100%);
*/  border: solid #4f4f4f 1px;




}



.tabs {


  border-radius: 7px;
}

.card {
  margin:0;
  border: none;
  border-radius:0;
  height: 100vh;

}



</style>
