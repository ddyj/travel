<template>
  <div>
   <cityheader></cityheader>
   <search></search>
  </div>
</template>

<script>
import cityheader from './components/cityheader.vue'
import search from './components/search.vue'
export default {
  name: 'city',
  components: {
    cityheader: cityheader,
    search: search
  }
}
</script>

<style lang="stylus" scoped></style>
