<template>
  <div>
    <AppNav />
    <Nuxt />
    <app-footer />
  </div>
</template>

<script>
import AppNav from '~/components/App/AppNav.vue'
import AppFooter from '~/components/AppFooter.vue'

export default {
  name: 'Layout',
  components: { AppNav, AppFooter },
}
</script>
