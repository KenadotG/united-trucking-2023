<template>
  <main>
    <AppHero />
    <app-features />
    <base-discovery />
    <BaseCompany />
  </main>
</template>

<script>
import AppFeatures from '~/components/AppFeatures.vue'
import BaseDiscovery from '~/components/Base/BaseDiscovery.vue'
import BaseCompany from '~/components/Base/BaseCompany.vue'

export default {
  name: 'IndexPage',
  components: { BaseCompany, AppFeatures, BaseDiscovery },
  data() {
    return {
      isHidden: false,
    }
  },
}
</script>
