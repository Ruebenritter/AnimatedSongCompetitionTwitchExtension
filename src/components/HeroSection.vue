
<template>
  <section class="hero">
    <div class="hero-content">
      <h1>Welcome to Twitch Game!</h1>
      <p>Learn the rules and get ready to play.</p>
      <button @click="startGame">Start New Game</button>
    </div>
  </section>
</template>

<script>
export default {
  name: 'HeroSection',
  created() {

  },
  data() {
    return {
    }
  },
  props: {
   
  },
  methods: {
   startGame() {
     this.$router.push('/game');
   }  
  },
}
</script>

<style lang="scss" scoped>
@import '../assets/base.css';
.hero {
  background-color: var(--primary-color);
  color: var(--text-color);
  padding: 2rem;
  text-align: center;
}
</style>

