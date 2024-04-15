
<script setup>
let socialIcons = ref({
  facebook: {
    value: "https://www.facebook.com/sergio.terrero/",
    icon:
        "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='1rem' height='1rem' viewBox='0 0 24 24'%3E%3Cpath fill='%23f7f7f7' d='M20.9 2H3.1A1.1 1.1 0 0 0 2 3.1v17.8A1.1 1.1 0 0 0 3.1 22h9.58v-7.75h-2.6v-3h2.6V9a3.64 3.64 0 0 1 3.88-4a20.26 20.26 0 0 1 2.33.12v2.7H17.3c-1.26 0-1.5.6-1.5 1.47v1.93h3l-.39 3H15.8V22h5.1a1.1 1.1 0 0 0 1.1-1.1V3.1A1.1 1.1 0 0 0 20.9 2'/%3E%3C/svg%3E",
  },
  instagram: {
    value:"https://www.instagram.com/sergio_terrero/",
    icon:
        "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='1rem' height='1rem' viewBox='0 0 15 15'%3E%3Cpath fill='%23f7f7f7' d='M7.5 5a2.5 2.5 0 1 0 0 5a2.5 2.5 0 0 0 0-5'/%3E%3Cpath fill='%23f7f7f7' fill-rule='evenodd' d='M4.5 0A4.5 4.5 0 0 0 0 4.5v6A4.5 4.5 0 0 0 4.5 15h6a4.5 4.5 0 0 0 4.5-4.5v-6A4.5 4.5 0 0 0 10.5 0zM4 7.5a3.5 3.5 0 1 1 7 0a3.5 3.5 0 0 1-7 0M11 4h1V3h-1z' clip-rule='evenodd'/%3E%3C/svg%3E",
  },

  twitter: {
    value: "https://twitter.com/Terrero28",
    icon:
        "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='1rem' height='1rem' viewBox='0 0 24 24'%3E%3Cg fill='%23f7f7f7'%3E%3Cpath d='M1 2h2.5L3.5 2h-2.5z'%3E%3Canimate fill='freeze' attributeName='d' dur='0.4s' values='M1 2h2.5L3.5 2h-2.5z;M1 2h2.5L18.5 22h-2.5z'/%3E%3C/path%3E%3Cpath d='M5.5 2h2.5L7.2 2h-2.5z'%3E%3Canimate fill='freeze' attributeName='d' dur='0.4s' values='M5.5 2h2.5L7.2 2h-2.5z;M5.5 2h2.5L23 22h-2.5z'/%3E%3C/path%3E%3Cpath d='M3 2h5v0h-5z' opacity='0'%3E%3Cset attributeName='opacity' begin='0.4s' to='1'/%3E%3Canimate fill='freeze' attributeName='d' begin='0.4s' dur='0.4s' values='M3 2h5v0h-5z;M3 2h5v2h-5z'/%3E%3C/path%3E%3Cpath d='M16 22h5v0h-5z' opacity='0'%3E%3Cset attributeName='opacity' begin='0.4s' to='1'/%3E%3Canimate fill='freeze' attributeName='d' begin='0.4s' dur='0.4s' values='M16 22h5v0h-5z;M16 22h5v-2h-5z'/%3E%3C/path%3E%3Cpath d='M18.5 2h3.5L22 2h-3.5z' opacity='0'%3E%3Cset attributeName='opacity' begin='0.5s' to='1'/%3E%3Canimate fill='freeze' attributeName='d' begin='0.5s' dur='0.4s' values='M18.5 2h3.5L22 2h-3.5z;M18.5 2h3.5L5 22h-3.5z'/%3E%3C/path%3E%3C/g%3E%3C/svg%3E",

  },

  linkedin: {
    value: "https://www.linkedin.com/in/sergio-terrero-34045a11b",
    icon:
      "data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='1rem' height='1rem' " +
      "viewBox='0 0 16 16'%3E%3Cpath fill='%23f5ebeb' d='M0 1.146C0 .513.526 0 1.175 0h13.65C15.474 0 16 .513 16 1.146v13.708c0 .633-.526 1.146-1.175 1" +
      ".146H1.175C.526 16 0 15.487 0 14.854zm4.943 12.248V6.169H2.542v7.225zm-1.2-8.212c.837 0 1.358-.554 1.358-1.248c-.015-.709-.52-1.248-1.342-1.248S2.4 " +
      "3.226 2.4 3.934c0 .694.521 1.248 1.327 1.248zm4.908 8.212V9.359c0-.216.016-.432.08-.586c.173-.431.568-.878 1.232-.878c.869 0 1.216.662 1.216 1.634v3." +
      "865h2.401V9.25c0-2.22-1.184-3.252-2.764-3.252c-1.274 0-1.845.7-2.165 1.193v.025h-.016l.016-.025V6.169h-2.4c.03.678 0 7.225 0 7.225z'/%3E%3C/svg%3E",
  },
});
</script>

<template>

    <div>
      <div class="social-icons" v-for="social in socialIcons">
       <a class="social" :href="social.value">
         <img :src="social.icon" class="icon" :alt="social.value"/>

       </a>




      </div>
    </div>
</template>

<style scoped>
.social-icons{
  display: inline-block;
}
.social img{
  height: 1.2rem;
}
.icon{
  margin: 0.5rem 0;
 margin-right:0.7rem;
}


</style>