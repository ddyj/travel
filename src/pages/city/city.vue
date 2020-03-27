<template>
  <div>
   <cityheader></cityheader>
   <search></search>
   <list></list>
   <Alphabet></Alphabet>
  </div>
</template>

<script>
import cityheader from './components/cityheader.vue'
import search from './components/search.vue'
import list from './components/list.vue'
import Alphabet from './components/Alphabet.vue'
export default {
  name: 'city',
  components: {
    cityheader: cityheader,
    search: search,
    list: list,
    Alphabet: Alphabet
  }
}
</script>

<style lang="stylus" scoped></style>
