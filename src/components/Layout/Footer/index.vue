<template>
  <footer v-if="showFooter" class="footer-section">
    <div class="footer-container">
      <div class="footer-left">
        <div class="logo-container">
          <img
            src="https://chlzslvdr.sirv.com/vuejs-bookmark/images/logo-bookmark-white.svg"
            alt="VueJS Bookmark"
          />
        </div>
        <nav class="footer-menu">
          <ul>
            <li><a href="#">Features</a></li>
            <li><a href="#">Pricing</a></li>
            <li><a href="#">Contact</a></li>
          </ul>
        </nav>
      </div>
      <div class="footer-right">
        <div class="social-icons">
          <a href="#" class="social-icon">
            <img
              src="https://chlzslvdr.sirv.com/vuejs-bookmark/images/icon-facebook.svg"
              alt="Facebook"
            />
          </a>
          <a href="#" class="social-icon">
            <img
              src="https://chlzslvdr.sirv.com/vuejs-bookmark/images/icon-twitter.svg"
              alt="Twitter"
            />
          </a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  props: {
    showFooter: {
      type: Boolean,
      default: true
    }
  }
}
</script>

<style lang="scss" scoped>
.footer-section {
  background-color: var(--neutral-dark-blue);
  padding: 2.5rem 10rem;
}

.footer-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.footer-left {
  display: flex;
}

.logo-container {
  margin-right: 4rem;
  align-items: center;
  display: flex;
}

.logo-container img {
  height: 2rem;
}

.footer-menu ul {
  list-style: none;
  display: flex;
  gap: 5rem;
  padding: 0;
  margin: 0;
}

.footer-menu ul li {
  margin: 0;
  text-transform: uppercase;
}

.footer-menu ul li a {
  text-decoration: none;
  color: var(--white);
  font-size: 1.4rem;
}

.footer-menu ul li a:hover {
  color: var(--primary-soft-red);
}

.social-icons {
  display: flex;
  gap: 4rem;
}

.social-icon img {
  height: 2rem;
  width: auto;
}

// .social-icon:hover img {
//   filter: invert(41%) sepia(87%) saturate(617%) hue-rotate(-33deg) brightness(95%) contrast(94%);
// }

@media (max-width: 768px) {
  .footer-section {
    padding: 10rem;
  }
}
</style>
