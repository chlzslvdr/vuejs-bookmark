<template>
  <header class="header-section">
    <div class="logo-container">
      <img
        src="https://chlzslvdr.sirv.com/vuejs-bookmark/images/logo-bookmark.svg"
        alt="VueJS Bookmark"
      />
    </div>
    <nav class="header-menu">
      <ul>
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
  name: 'Header'
}
</script>

<style lang="scss" scoped>
@import '@scss/mixins';

.header-section {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 2rem;
  background-color: var(--white);
}

.logo-container img {
  height: 3rem;
}

.header-menu ul {
  list-style: none;
  display: flex;
  gap: 2rem;
  padding: 0;
  margin: 0;
  text-transform: uppercase;
  align-items: center;
}

.header-menu ul li {
  margin: 0;
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

@include respond(tab-port) {
  .header-section {
    padding: 3rem 10rem;
  }

  .header-menu ul {
    gap: 4rem;
  }

  .header-menu ul li a {
    font-size: 1.6rem;
  }

  .login-button {
    padding: 1rem 3.2rem;
  }
}

@media (min-width: 1024px) {
  .header-section {
    padding: 1rem 15rem;
  }

  .header-menu ul {
    gap: 6rem;
  }

  .header-menu ul li a {
    font-size: 1.6rem;
  }

  .login-button {
    padding: 1rem 3.2rem;
  }
}
</style>
