<template>
  <div class="CharacterIntroduction">
    <button @click="changeTileColor">Change Tile Color</button>
    <div id="tiles">
      <div class="tile" v-for="index in tileAmount" :key="index">

      </div>
    </div>

    <!-- Player Portrait Image -->
    <img class="player-portrait" :src="playerPortrait" alt="Player Portrait">
  </div>
</template>

<script>
  import anime from 'animejs/lib/anime.es.js';

  export default {
    name: 'CharacterIntroduction',
    created() {

    },
    data() {
      var character = null;
      var player = null;
      var wrapper = document.getElementById('tiles');
      var playerPortrait = '/images/cat_protrait.png';
      return {
        character,
        player,
        wrapper,
        playerPortrait

      }
    },
    props: {

    },
    methods: {
      changeTileColor() {
        anime({
          targets: ".tile",
          backgroundColor: '#ff4b2b',
          delay: anime.stagger(20, {
            grid: [this.getColumns, this.getRows],
            from: 'first',
          })
        });
        anime({
          targets: ".player-portrait",
          translateX:{
            value: 600,
            direction: 'alternate',
            duration: 2000,
            easing: 'linear'
          }
        })
      }
    },
    computed: {
      getRows() {
        return Math.floor(document.body.clientHeight / this.getSize);
      },
      getColumns() {
        return Math.floor(document.body.clientWidth / this.getSize);
      },
      tileAmount() {
        return this.getRows * this.getColumns;
      },
      getSize() {
        return document.body.clientWidth > 800 ? 32 : 16;
      }
    }
  }
</script>

<style lang="scss" scoped>
  @import '../assets/base.css';

  .CharacterIntroduction {
    background-color: var(--background-color);
    height: 100%;
    width: 100%;
    overflow: hidden;
    margin: 0px;
    position: relative;
  }

  #tiles {
    height: 100vh;
    width: 100vw;

    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(32px, 1fr));
    grid-template-rows: repeat(auto-fit, minmax(32px, 1fr));
    //gap: 16px;
  }

  .tile {
    background-color: var(--accent-color);
  }

  .player-portrait{
    position: absolute;
    height: 95%;
    left: -10%;
    bottom: 0;
  }

</style>