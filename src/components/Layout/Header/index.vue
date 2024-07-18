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
        src="https://chlzslvdr.sirv.com/vuejs-bookmark/images/icon-hamburger.svg"
        alt="menu"
        @click="toggleMenu"
      />
      <ul :class="{ open: isMenuOpen }">
        <li><a href="#">Features</a></li>
        <li><a href="#">Pricing</a></li>
        <li><a href="#">Contact</a></li>
        <li><button class="login-button">Login</button></li>
      </ul>
    </nav>
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
}

.mobile-menu-toggle {
  cursor: pointer;
  display: none;
}

.header-menu ul {
  display: flex;
  list-style: none;
  padding: 0;
  margin: 0;
  text-transform: uppercase;
  gap: 2rem;
}

.header-menu ul.open {
  display: block;
  position: absolute;
  top: 100%;
  left: 0;
  background-color: var(--white);
  width: 100%;
  text-align: center;
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

@media (max-width: 768px) {
  .header-section {
    padding: 3rem 5rem;
  }

  .mobile-menu-toggle {
    display: block;
  }

  .header-menu ul {
    display: none;
    flex-direction: column;
  }

  .header-menu ul.open {
    display: block;
  }
}
</style>
