<template>
  <Header />
  <slot />
  <Footer />
</template>

<script>
import Header from './Header/index.vue'
import Footer from './Footer/index.vue'

export default {
  name: 'Layout',
  components: {
    Header,
    Footer
  }
}
</script>
