<script setup lang="ts">

</script>

<template>
  <div>
    <UContainer class="main-container ">
      <div class="main-wrapper">

        <UIHeader/>
        <UITabs/>

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
  background: linear-gradient(175deg, rgb(6, 21, 43) 0%, rgb(26, 36, 44) 46%, rgb(23, 89, 119) 95%);
  border: solid #4f4f4f 1px;

}

@media only screen and (min-width: 1080px) {
  .main-container {
    min-width: 47%;
  }
}

@media only screen and (max-width: 450px) {
  .main-container  {
    padding: 0;
  }

  .main-wrapper {
    margin: 0 auto;
    border-radius: 0;
  }
}

</style>
