<template src="../static/theme/base/mainpage.html"></template>

<script>
import ProfileView from '@/components/ProfileComponent.vue'
import BiographyComponent from '@/components/BiographyComponent.vue'
import EducationComponent from '@/components/EducationComponent.vue'
import EmploymentComponent from '@/components/EmploymentComponent.vue'
import HonorsComponent from '@/components/HonorsComponent.vue'
import SkillsComponent from '@/components/SkillsComponent.vue'
import PortfolioComponent from '@/components/PortfolioComponent.vue'
import LanguagesComponent from '@/components/LanguagesComponent.vue'
export default {
  name: 'top-page',
  components: {
    ProfileView,
    BiographyComponent,
    EducationComponent,
    EmploymentComponent,
    HonorsComponent,
    SkillsComponent,
    PortfolioComponent,
    LanguagesComponent
  },
  created () {
    this.$store.dispatch('loadCV')
  },
  data () {
    return {
      menuVisible: false
    }
  },
  methods: {
    displaySection (title) {
      return this.$store.getters.displaySection(title)
    }
  }
}
</script>

<style>
body {
  font-family: 'Raleway', sans-serif;
}
.fade-enter-active, .fade-leave-active {
  transition: opacity .33s
}
.fade-enter, .fade-leave-to {
  opacity: .3
}
</style>
