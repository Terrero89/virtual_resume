
<script setup lang="ts">

const items = [{

  key: 'About ',
  label: 'About me',
 description: 'Information About me etc...Information about education etc..' +
      'Information about education etc..Information about education etc..Information About me etc...Information about education etc..' +
      'Information about education etc..Information about education etc..Information About me etc...Information about education etc..' +
      'Information about education etc..Information about education etc..'
}, {
  key: 'Education',
  label: 'Education',
  description: 'Information about education etc..'
}, {
  label: 'Skills',
  key: 'Technologies',
  description: 'Skills highlighted by used etc.. ',
  tech: ["Go", "Java", "Pearl", "Javascript", "React", "Vue"]
}, {
  label: 'Experience',
  key:'What I know',
  description:'And, this is the content for Tab2'
},]
</script>

<template>
  <div>

    <UContainer>
      <div class="main-wrapper">
        <div class="header-section">
          <div class="img-container">
            <img
                src="~/public/Sergio%20Terrero.jpg"
                class="header-image">
          </div>


          <div class="header-text">
            <h3>Sergio Terrero</h3>
            <p>Software Engineer</p>

          </div>


        </div>
        <div class="tabs">
          <UTabs :items="items" class="w-full">
            <template #item="{ item }">
              <UCard class="card">
                <template #header>
                  <p class="text-base font-semibold leading-6 text-gray-900 dark:text-white">
                    {{ item.key }}
                  </p>
                  <p class="mt-1 text-sm text-gray-500 dark:text-gray-400">
                    {{ item.description }}
                  </p>
                  <div v-for="t in item.tech" class="mt-1 text-sm text-gray-500 dark:text-gray-400">
                    {{ t}}
                  </div>
                </template>




                </UCard>


            </template>
          </UTabs>
        </div>

      </div>

    </UContainer>

  </div>
</template>


<style scoped>
.main-wrapper {
  background-color: #8f8f8f;
  border: solid #000000 1px;
  height: 95vh;
  border-radius: 7px;
  margin: 1rem auto;
}

.header-section {
  //border: solid #737373 1px;
  border-radius: 7px;
  padding: 2rem;
  max-height: 20rem;
  background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.8)), url("https://www.bostonintransit.com/cdn/shop/products/HistoricalMBTAMap-2022MediumPrint-web.jpg?v=1669156236");
  background-position: center;
  object-fit: cover;
  background-repeat: no-repeat;
  background-size: auto;
  align-content: center;
  align-items: center;
}

.img-container {
  border-radius: 50%;
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
border: solid #d9d9d9 1px;
  object-fit: cover ;
  margin: 0 auto;
  background-position: center;
  background-repeat: no-repeat;
  -moz-background-size: cover;
  background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.8)), url("https://www.bostonintransit.com/cdn/shop/products/HistoricalMBTAMap-2022MediumPrint-web.jpg?v=1669156236");




}

.header-text {
  text-align: center;
width: 15rem;

  margin: 1rem  auto;

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

.tabs{
  height: 61%;

  border-radius: 7px;

}

.card{
border: none;
  margin: 0.5rem auto;
  min-height: 100%;
}
</style>
