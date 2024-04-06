<template>
  <div>
    <div class="header-section">
      <div class="img-container">

        <img src="~/public/sergioTerrero.png" class="header-image" alt="my-avatar" />
      </div>

      <div class="header-text">
        <h3>Sergio Terrero</h3>
        <p>Software Engineer</p>
      </div>
    </div>
  </div>
</template>

<style scoped>


.header-section {

  padding: 2rem;
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

  object-fit: contain;
  margin: 0 auto;
  background-position: center;
  background-repeat: no-repeat;
  -moz-background-size: cover;
  background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.8)),
  url("https://www.bostonintransit.com/cdn/shop/products/HistoricalMBTAMap-2022MediumPrint-web.jpg?v=1669156236");
}
@media only screen and (max-width:450px){
  .img-container img {
    border-radius: 50%;

    width: 10rem;
    height: 10rem;

   margin: 1rem auto;
  }

  .header-text {
    text-align: center;
    width: 15rem;

    margin: 1rem auto;
  }
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
</style>