
<template>
  <div class="GameViewFrame">
   <CharacterIntroduction/>
  </div>
</template>

<script>
import CharacterIntroduction from '../components/CharacterIntroduction.vue';

export default {
  name: 'GameView',
  created() {

  },
  data() {
    return {
    }
  },
  props: {
   
  },
  methods: {
   
  },
  components: {
    CharacterIntroduction,
  }
}
</script>

<style lang="scss" scoped>
.GameViewFrame{
  background-color: var(--background-color);
  width: 100%;
}
</style>

