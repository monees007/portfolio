<script setup>
import { RouterView } from 'vue-router'
import Sidebar from '@/components/SideBar.vue'
</script>

<template>
  <nav class="navbar">
    <ul class="navbar-list">
      <RouterLink class="navbar-link navbar-item" to="/">About</RouterLink>
      <RouterLink class="navbar-link navbar-item" to="/resume">Resume</RouterLink>
      <RouterLink class="navbar-link navbar-item" to="/projects">Projects</RouterLink>
      <RouterLink class="navbar-link navbar-item" to="/experiments">Experiments</RouterLink>
      <RouterLink class="navbar-link navbar-item" to="/blogs">Blogs</RouterLink>
      <RouterLink class="navbar-link navbar-item" to="/contact">Contact</RouterLink>
    </ul>
  </nav>

  <gbox>
    <Sidebar style="max-height: max-content" class="main" />
<!--    <article style="" class="">-->
      <RouterView style="" class="main" />
<!--    </article>-->


  </gbox>
</template>

<style>
header {
  line-height: 1.5;
  //max-height: 100vh;
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
  color: wheat;
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
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}


@media (max-width: 580px) {

  gbox {
    display: flex;
    flex-direction: column;
  }
  article, sidebar{
    margin: 4px !important;
    width: auto;
  }

  .clients-item {
    min-width: calc(33.33% - 10px);
  }

  .navbar-list {
    display: flex;
    flex-direction: row;
  }

  .project-img,
  .blog-banner-box {
    height: auto;
    width: auto;
  }

}


@media (min-width: 580px) {

  :root {
    --fs-1: 32px;
    --fs-2: 24px;
    --fs-3: 26px;
    --fs-4: 18px;
    --fs-6: 15px;
    --fs-7: 15px;
    --fs-8: 12px;

  }

  article {
    margin-top: 100px;
    //margin-bottom: 100px;

  }

  gbox {
    display: flex;
    flex-direction: row;
    align-items: center;
    min-height: 100vh;

  }

  .navbar {
    margin-top: 0;
    position: fixed;
    top: 0;
    right: auto;
    left: 0;

  }
}

</style>
