<script setup>
import { RouterLink, RouterView } from 'vue-router'
import PersistentHeader from './components/PersistentHeader.vue';


</script>

<template>
  <header>
    <PersistentHeader/>
  </header>
    <div class="frame">
      <RouterView />
    </div>
</template>


<style scoped lang="scss">
.frame{
  height: 100%;
  width: 100%;
  display: flex;
}
</style>