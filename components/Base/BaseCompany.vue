<template>
  <div
    class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8 pt-20 pb-16 text-center lg:pt-32"
  >
    <div>
      <p class="mx-10 text-lg tracking-tight text-slate-700">
        Trusted by these companies so far
      </p>
    </div>
    <ul class="flex">
      <li class="p-10 m-10" v-for="image in images" :key="image.path">
        <img :src="image.path" :alt="image.alts" />
      </li>
    </ul>
  </div>
</template>

<script>
const imageLists = [
  {
    path: '/img/Dangote-Logo.jpg',
    alts: 'Logo 1',
  },
  {
    path: '/img/Dangote-Logo.jpg',
    alts: 'Logo 2',
  },
  {
    path: '/img/Dangote-Logo.jpg',
    alts: 'Logo 2',
  },
  {
    path: '/img/Dangote-Logo.jpg',
    alts: 'Logo 2',
  },
  {
    path: '/img/Dangote-Logo.jpg',
    alts: 'Logo 2',
  },
  {
    path: '/img/Dangote-Logo.jpg',
    alts: 'Logo 2',
  },
]
export default {
  name: 'BaseCompany',
  data() {
    return {
      images: imageLists,
    }
  },
}
</script>
