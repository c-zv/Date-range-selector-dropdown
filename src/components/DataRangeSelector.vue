<template>
  <div>
    <h3>Date range selector dropdown button</h3>
    <div class="rangeContainer">
      <b-button icon-left="chevron-left" />
      <b-datepicker
        v-model="date"
        @input="onDateChange"
        ref="datepicker"
        placeholder="Click to select a date range"
        locale="en-GB"
        position="is-bottom-left"
        show-week-number
        editable
        range
      >
        <template v-slot:default>
          <div class="selectorFooter">
            <b-button @click="onYearToDate">Year to date</b-button>
            <b-button @click="onMonthToDate">Month to date</b-button>
          </div>
        </template>
      </b-datepicker>
      <b-button icon-right="chevron-right" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'DataRangeSelector',
  data () {
    return {
      date: null
    }
  },
  methods: {
    onDateChange () {
      this.$emit('input', this.date)
    },
    onYearToDate () {
      const now = new Date()
      this.date = [new Date(now.getFullYear(), 0, 1), now]
      this.onDateChange()
      this.$refs.datepicker.toggle()
    },
    onMonthToDate () {
      const now = new Date()
      this.date = [new Date(now.getFullYear(), now.getMonth(), 1), now]
      this.onDateChange()
      this.$refs.datepicker.toggle()
    }
  }
}
</script>

<style scoped lang="scss">
.rangeContainer {
  display: flex;
  flex-direction: row;
  justify-content: center;
}

.selectorFooter {
  display: flex;
  justify-content: space-evenly;
}

</style>
