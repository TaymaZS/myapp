<template>
  <nav>
    <router-link to="/">Главная</router-link> |
    <router-link to="/about">About</router-link>
    <router-link to="/KatalogComponent">Каталог</router-link>
  </nav>
  <router-view/>
</template>

<style>
body {
  background-color: rgb(71, 71, 202);
}
  *{
    margin: 0;
  }
  nav {
    background-color: silver;
    width: 100%;
    height: 40px;
    font-size: 20px;
  }
  nav router-view {
    text-decoration: none;
  }
</style>
