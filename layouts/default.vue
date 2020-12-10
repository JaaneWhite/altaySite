<template>
  <div>
    <header-component />
    <Nuxt />
  </div>
</template>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,300&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Oswald:wght@200;300;400;500;600;700&display=swap');

@media (min-width: 1500px) {
  .container {
    max-width: 1460px;
  }
}
/* по умолчанию -  мобильная версия - 0 - 767 px*/
@media (min-width: 0) {
  body {
    margin: auto;
    font-family: Roboto, sans-serif;
    color: #343f44;
  }
  .row {
    padding: 0;
    margin: 0;
  }
  .container {
    padding: 0;
  }
  a {
    color: #343f44;
    &:hover {
      color: #9783a6
    }
  }
}


</style>
<script>
import HeaderComponent from "~/components/HeaderComponent";
export default {
  components: {HeaderComponent}
}
</script>
