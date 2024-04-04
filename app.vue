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
        <div class="header-section">
          <div class="img-container">

            <img src="~/public/sergioTerrero.png" class="header-image" alt="my-avatar" />
          </div>

          <div class="header-text">
            <h3>Sergio Terrero</h3>
            <p>Software Engineer</p>
          </div>
        </div>

<UITabs/>
<!--        <UISidebar/>-->
      </div>
    </UContainer>
  </div>
</template>

<style scoped>

.co{
//min-width: 70%;
}
@media only screen and (min-width:1080px){
.co{
  min-width: 60%;
}
}

@media only screen and (min-width:768px){
  .tabs{
   display: none
  }
  .side{

  }
}
@media only screen and (max-width:768px){

  .side-vertical{
display: none;
  }
}
.main-wrapper {
min-height: 90vh;
  background-color: #8f8f8f;
  border: solid #4f4f4f 1px;

  border-radius: 7px;
  margin: 1rem auto;

}

.header-section {
  border: solid #737373 1px;

  padding: 2rem;
  max-height: 20rem;
  background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.8)),
    url("https://www.bostonintransit.com/cdn/shop/products/HistoricalMBTAMap-2022MediumPrint-web.jpg?v=1669156236");
  background-position: center;
  object-fit: cover;
  background-repeat: no-repeat;
  background-size: auto;
  align-content: center;
  align-items: center;

}

.img-container {

  width: 12rem;
  height: 12rem;
  margin: 0 auto;

  background-position: center;
  background-repeat: no-repeat;
  -moz-background-size: cover;
}

.img-container img {
  border-radius: 50%;

  width: 12rem;
  height: 12rem;
  //border: solid #d9d9d9 1px;
  object-fit: contain;
  margin: 0 auto;
  background-position: center;
  background-repeat: no-repeat;
  -moz-background-size: cover;
  background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.8)),
    url("https://www.bostonintransit.com/cdn/shop/products/HistoricalMBTAMap-2022MediumPrint-web.jpg?v=1669156236");
}

.header-text {
  text-align: center;
  width: 15rem;

  margin: 1rem auto;
}

.header-text h3 {
  font-weight: 600;
  font-size: 2rem;
  color: #bdbdbd;
}
.header-text p {
  font-weight: 600;
  font-size: 1rem;
  color: #bdbdbd;
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
