<template>
  <header>
    <nav>
      <ul>
        <li><nuxt-link to="/">Starting page</nuxt-link></li>
        <li><nuxt-link to="/recipes">Recipes</nuxt-link></li>
        <li><nuxt-link to="/about">About</nuxt-link></li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>
header {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 30px;
  background-color: #521751;
}

ul {
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  list-style: none;
}

li {
  margin: 0 10px;
}

a {
  text-decoration: none;
  color: white;
}
</style>

