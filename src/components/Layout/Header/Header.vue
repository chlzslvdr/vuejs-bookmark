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

<style scoped>
.header-section {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 30px 250px;
  background-color: var(--white);
}

.logo-container img {
  height: 30px;
}

.header-menu ul {
  list-style: none;
  display: flex;
  gap: 60px;
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
  font-size: 16px;
}

.header-menu ul li a:hover {
  color: var(--primary-soft-red);
}

.login-button {
  background-color: var(--primary-soft-red);
  color: var(--white);
  border: none;
  padding: 10px 32px;
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
</style>
