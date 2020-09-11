<template>
  <b-datepicker
    placeholder="Click to select a date range"
    show-week-number
    locale="en-GB"
    range
    v-bind="$props"
    v-on="$listeners"
  >
  </b-datepicker>
</template>

<script>
export default {
  name: 'DataRangeSelector'
}
</script>

<style scoped lang="scss">

</style>
