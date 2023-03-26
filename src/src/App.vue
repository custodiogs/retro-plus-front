<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HeaderMenu from './components/HeaderMenu.vue'
</script>

<template>
  <header>
      <HeaderMenu msg="Retro Plus" />

      <!-- <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav> -->
  </header> 
  <main><RouterView /></main>
  
</template>
<style scoped>

header {
  background-color: #f1f1f1;
  /* line-height: 1.5; */
  height: 8vh;  
  position: fixed;
  top:0;
  width: 100%;  
  padding: 5px 5px 5px 30px;
}
main{
position:relative;
justify-content: space-between;
padding-top: 10px;
padding-left: 15px;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
} 

@media (min-width: 1024px) {
  header {
    position: relative;
    display: flex;
    place-items: center; 
    justify-content: space-between;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
