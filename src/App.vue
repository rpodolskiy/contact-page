<template>
  <ContactUs />
</template>

<script>
import ContactUs from './components/ContactUs.vue'

export default {
  name: 'App',
  components: {
    ContactUs
  }
}
</script>

<style>
  #app {
    text-align: center;
    margin-top: 60px;
    background: url("../public/img/dots.svg");
    background-position: right;
    background-repeat: no-repeat;
  }
  body {
    margin: 0;
  }
</style>
