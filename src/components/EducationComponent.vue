<template src="../../static/theme/base/education.html"></template>

<script>
import TimelineView from './TimelineComponent'
export default {
  data () {
    return {
      education: this.$store.getters.getSection('education')
    }
  },
  components: {'TimelineView': TimelineView}
}
</script>

<style scoped>
</style>
