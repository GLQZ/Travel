<template>
  <div>
    <city-header></city-header>
    <city-search></city-search>
  </div>
</template>

<script type="text/ecmascript-6">
import CityHeader from './components/Header.vue'
import CitySearch from './components/search.vue'
export default {
  name: 'City',
  components: {
    CityHeader,
    CitySearch
  }
}
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
</style>
