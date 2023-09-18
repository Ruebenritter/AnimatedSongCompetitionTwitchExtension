
<template>
  
  <HeroSection/>
  <LoginOptions/>
</template>

<script>
import HeroSection from '../components/HeroSection.vue';
import LoginOptions from '../components/LoginOptions.vue';

export default {
  name: 'LandingPage',
  components:{
    HeroSection,
    LoginOptions,
    
  }
};

</script>

<style scoped>
 body {
  font-family: Arial, sans-serif;
  background-color: #f4f4f4;
  margin: 0;
  padding: 0;
}

.header {
  background-color: #2a2a2a;
  color: #ffffff;
  padding: 1rem;
  text-align: center;
}



.login-options {
  background-color: #ffffff;
  padding: 2rem;
  text-align: center;
}
</style>