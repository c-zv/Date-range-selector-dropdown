<template>
  <div class="container">
    <data-range-selector
      v-model="datesRange"
    />
  </div>
</template>

<script>
import DataRangeSelector from '@/components/DataRangeSelector.vue'
export default {
  name: 'Home',
  components: {
    DataRangeSelector
  },
  data () {
    return {
      datesRange: []
    }
  }
}
</script>
