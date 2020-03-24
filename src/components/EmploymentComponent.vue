<template src="../../static/theme/base/employment.html"></template>

<script>
import TimelineView from './TimelineComponent'
export default {
  components: {'TimelineView': TimelineView},
  data () {
    return {
      collapse: []
    }
  },
  computed: {
    employment () {
      for (var item in this.$store.getters.getSection('employment').items) {
        this.collapse.push(false)
        item = item + 0
      }
      return this.$store.getters.getSection('employment')
    }
  },
  methods: {
    toggleCourses (index) {
      this.$set(this.collapse, index, !this.collapse[index])
    },
    isVisible (index) {
      return this.collapse[index]
    }
  }
}
</script>

<style scoped>

</style>
