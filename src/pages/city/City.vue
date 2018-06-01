<template>
  <div>
    <city-header></city-header>
    <city-search></city-search>
    <city-list></city-list>
    <city-alphabet></city-alphabet>
  </div>
</template>

<script type="text/ecmascript-6">
import CityHeader from './components/Header.vue'
import CitySearch from './components/search.vue'
import CityList from './components/list.vue'
import CityAlphabet from './components/Alphabet.vue'
export default {
  name: 'City',
  components: {
    CityHeader,
    CitySearch,
    CityList,
    CityAlphabet
  }
}
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
</style>
