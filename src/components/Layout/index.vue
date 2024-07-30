<template>
  <div class="layout-container">
    <Header @update:showFooter="updateFooterVisibility" />
    <main class="main-section">
      <slot />
    </main>
    <!-- <div class="author">
      Challenge by Frontend Mentor. Coded by
      <a class="author-link" href="https://github.com/chlzslvdr" target="_blank"
        >Chelzea Salvador</a
      >
    </div> -->
    <Footer :showFooter="showFooter" />
  </div>
</template>

<script>
import Header from './Header/index.vue'
import Footer from './Footer/index.vue'

export default {
  name: 'Layout',
  components: {
    Header,
    Footer
  },
  data() {
    return {
      showFooter: true
    }
  },
  methods: {
    updateFooterVisibility(isVisible) {
      this.showFooter = isVisible
    }
  }
}
</script>

<style lang="scss">
.layout-container {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.main-section {
  flex: 1;
}

.author {
  text-align: center;
  font-size: 1rem;
}

.author-link {
  cursor: pointer;
  color: var(--neutral-dark-blue);
  text-decoration: none;
  font-weight: bold;
}
</style>
