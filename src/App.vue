<template>
  <div class="container">
    <div class="row">
      <card-info></card-info>
    </div>
  </div>
</template>

<script>
import CardInfo from "./components/CardInfo.vue";

export default {
  name: 'App',
  components: {
    CardInfo
  }
}
</script>

<style lang="scss">
* {
  padding: 0;
  margin: 0;
}

body {
  padding-left: 15px;
  padding-right: 15px;
}

#app {
  font-family: 'Source Sans Pro', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;

  h1, h2, h3, h4, h5, h6 {
     font-family: 'Playfair Display', serif;
     font-weight: 700;
  }
}

.container {
  background-color: #eaf0f5;
  padding: 30px 20px;
  box-shadow: rgba(14, 30, 37, 0.12) 0px 2px 4px 0px, rgba(14, 30, 37, 0.32) 0px 2px 16px 0px;
  border-radius: 7px;

  @media only screen and (min-width: 1200px) {
    max-width: 1300px;
  }
}
</style>
