<template>
  <header class="header-section">
    <div class="logo-container">
      <img
        src="https://chlzslvdr.sirv.com/vuejs-bookmark/images/logo-bookmark.svg"
        alt="VueJS Bookmark"
      />
    </div>
    <nav class="header-menu">
      <img
        class="mobile-menu-toggle"
        :src="
          isMenuOpen ? '' : 'https://chlzslvdr.sirv.com/vuejs-bookmark/images/icon-hamburger.svg'
        "
        alt="menu"
        @click="toggleMenu"
        v-if="!isMenuOpen"
      />
      <ul>
        <li><a href="#">Features</a></li>
        <li><a href="#">Pricing</a></li>
        <li><a href="#">Contact</a></li>
        <li><button class="login-button">Login</button></li>
      </ul>
    </nav>
    <div :class="{ overlay: isMenuOpen }" class="menu-overlay">
      <div class="overlay-header">
        <div class="logo-container">
          <img
            src="https://chlzslvdr.sirv.com/vuejs-bookmark/images/logo-bookmark-white.svg"
            alt="VueJS Bookmark"
          />
        </div>
        <img
          class="mobile-menu-toggle"
          src="https://chlzslvdr.sirv.com/vuejs-bookmark/images/icon-close.svg"
          alt="close menu"
          @click="toggleMenu"
        />
      </div>
      <div class="overlay-content">
        <ul @click="toggleMenu">
          <li><a href="#">Features</a></li>
          <li><a href="#">Pricing</a></li>
          <li><a href="#">Contact</a></li>
          <li><button class="login-button">Login</button></li>
        </ul>
        <div class="social-icons">
          <a href="#">
            <img
              src="https://chlzslvdr.sirv.com/vuejs-bookmark/images/icon-facebook.svg"
              alt="Facebook"
            />
          </a>
          <a href="#">
            <img
              src="https://chlzslvdr.sirv.com/vuejs-bookmark/images/icon-twitter.svg"
              alt="Twitter"
            />
          </a>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      isMenuOpen: false
    }
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen
      this.$emit('update:showFooter', !this.isMenuOpen)
    }
  }
}
</script>

<style lang="scss" scoped>
.header-section {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 2rem 10rem;
  background-color: var(--white);
}

.logo-container img {
  height: 3rem;
}

.header-menu {
  position: relative;
  z-index: 11;
}

.mobile-menu-toggle {
  cursor: pointer;
  display: none;
  z-index: 12;
}

.header-menu ul {
  display: flex;
  list-style: none;
  padding: 0;
  margin: 0;
  text-transform: uppercase;
  gap: 2rem;
}

.header-menu ul li {
  margin: 1rem;
}

.header-menu ul li a {
  text-decoration: none;
  color: var(--neutral-dark-blue);
  font-size: 1.4rem;
}

.header-menu ul li a:hover {
  color: var(--primary-soft-red);
}

.login-button {
  box-sizing: border-box;
  background-color: var(--primary-soft-red);
  color: var(--white);
  border: none;
  padding: 8px 2.4rem;
  border-radius: 4px;
  cursor: pointer;
  font-weight: 600;
  text-transform: uppercase;
}

.login-button:hover {
  background-color: var(--white);
  color: var(--primary-soft-red);
  border: 2px solid var(--primary-soft-red);
}

.menu-overlay {
  display: none;
}

.menu-overlay.overlay {
  display: flex;
  flex-direction: column;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(47, 53, 79, 0.9);
  z-index: 10;
}

.overlay-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  padding: 1rem 2rem;
}

.overlay-header .logo-container img {
  height: 3rem;
}

.overlay-header .mobile-menu-toggle {
  cursor: pointer;
  display: block;
}

.overlay-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2rem;
  color: var(--white);
  margin-top: 3rem;
}

.overlay-content ul {
  display: flex;
  flex-direction: column;
  align-items: center;
  list-style: none;
  padding: 0;
  margin: 0;
  gap: 1rem;
  text-transform: uppercase;
}

.overlay-content ul li a {
  color: var(--white);
  font-size: 1.4rem;
  text-decoration: none;
}

.overlay-content ul li a:hover {
  color: var(--primary-soft-red);
}

.social-icons {
  display: flex;
  gap: 1rem;
}

.social-icons img {
  width: 2rem;
  height: 2rem;
}

@media (max-width: 768px) {
  .header-section {
    padding: 3rem 5rem;
  }

  .mobile-menu-toggle {
    display: block;
  }

  .header-menu ul {
    display: none;
  }

  .menu-overlay {
    display: none;
  }

  .menu-overlay.overlay {
    display: flex;
  }

  .login-button {
    background-color: transparent;
    border: 1px solid white;
    color: white;
  }
}
</style>
