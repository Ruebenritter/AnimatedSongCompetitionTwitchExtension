
<template>
  <div class="banner">
   <h1>Rübi's Animated Song Competition</h1>
   <div class="icon"></div>
  </div>
</template>

<script>
export default {
  name: 'PersistentHeader',
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
}
</script>

<style lang="scss" scoped>
.banner{
  border: 1px solid var(--accent-color);
  display: flex;
}

.icon{
  border-radius: 20px;
  border: 1px solid var(--primary-color);
  width: 40px;
  height: 40px;
  align-self: center;
}
</style>

