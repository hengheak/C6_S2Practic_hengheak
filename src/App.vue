<template>
  <Navbar></Navbar>
  <Form></Form>
</template>

<script>
import Navbar from './components/NavbarView.vue';
import Form from './components/FormView.vue';

export default {
  components:{
     Navbar,
     Form,

  }
 
}
</script>

<style>
#app {
   font-family: sans-serif;
}

</style>
