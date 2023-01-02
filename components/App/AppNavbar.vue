<template>
  <nav class="py-5 px-40 shadow-lg flex justify-between items-center">
    <ul class="flex space-x-6">
      <li v-for="item in menus" :key="item.name">
        <a :href="item.link">{{ item.name }}</a>
      </li>
    </ul>
    <div>
      <h2 class="flex">{{ message }}</h2>
      <button
        @click="buttonClick()"
        class="px-[16px] py-[7px] border rounded-full hover:border hover:border-gray-500"
      >
        {{ logged ? 'Sign in' : ' sing out' }}
      </button>
    </div>
  </nav>
</template>

<script>
const menusItems = [
  {
    name: 'Home',
    link: '/',
  },
  {
    name: 'About',
    link: '/about',
  },

  {
    name: 'Contact',
    link: '/contact',
  },
  {
    name: 'FAQs',
    link: '/faqs',
  },
]
export default {
  name: 'AppNavbar',
  data() {
    return {
      message: 'User is not logged',
      logged: false,
      menus: menusItems,
    }
  },
  /*  computed: {
    log() {
      return this.logged ? 'Sign up' : ' sing out'
    },
  }, */
  // mounted() {
  // this.message = 'hi'
  //  },

  methods: {
    buttonClick() {
      // console.log('here')
      this.message = 'User is logged'
      this.logged = !this.logged
      //   this.menus = this.menus.push({ name: 'Product', link: '/product' })
    },
  },
}
</script>
