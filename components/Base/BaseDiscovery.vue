<template>
  <div class="bg-blue-500 py-10 sm:py-14 lg:py-22">
    <div class="my-10 px-40 w-full mx-auto text-center">
      <h1
        class="max-w-4xl font-display text-7xl font-medium tracking-tight text-white sm:text-5xl"
      >
        Special Deals and Best Routes
      </h1>
      <p class="mx-auto mt-6 max-w-2xl text-lg tracking-tight text-indigo-50">
        Book a special routes at a great price! Grab a last minute offer with
        get forth and back trip.
      </p>
    </div>
    <div class="mx-auto max-w-xl px-6 lg:max-w-7xl lg:px-8">
      <h2 class="sr-only">A better way to send money.</h2>
      <dl class="grid grid-cols-1 gap-16 lg:grid lg:grid-cols-3">
        <div v-for="discovery in discoveries" :key="discovery.name">
          <dt>
            <div
              class="flex items-center justify-center rounded-xl bg-indigo-500 text-white"
            >
              <img :src="discovery.srcs" :alt="discovery.alts" />
            </div>
            <p
              class="mt-6 text-lg font-semibold leading-8 tracking-tight text-white"
            >
              {{ discovery.name }}
            </p>
          </dt>
          <dd class="mt-2 text-base leading-7 text-indigo-50">
            {{ discovery.description }}
          </dd>
        </div>
      </dl>
    </div>
  </div>
</template>
<script>
const discoveryList = [
  {
    name: 'Wolega Adventures',
    description:
      'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Maiores impedit perferendis suscipit eaque, iste dolor cupiditate blanditiis ratione.',
    srcs: '/img/road-img-2.jpg',
    alts: 'Wolega Road',
  },
  {
    name: 'Kamashi Minerals',
    description:
      'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Maiores impedit perferendis suscipit eaque, iste dolor cupiditate blanditiis ratione.',
    srcs: '/img/coal-Img-2.jpg',
    alts: 'Char Coal',
  },
  {
    name: 'Marble Transportation',
    description:
      'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Maiores impedit perferendis suscipit eaque, iste dolor cupiditate blanditiis ratione.',
    srcs: '/img/marble-img-2.jpg',
    alts: 'White Marble',
  },
]
export default {
  name: 'BaseDiscovery',
  data() {
    return {
      discoveries: discoveryList,
    }
  },
}
</script>
