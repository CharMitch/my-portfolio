<template>
  <div id="app">
    <header>
      <h1>Charlene M. Mitchell</h1>
      <nav>
        <router-link to="/">Home</router-link> |
        <router-link to="/about">About</router-link> |
        <router-link :to="{ name: 'portfolio-view' }">Portfolio</router-link> |
        <router-link :to="{ name: 'resume-view' }">Resume</router-link>
      </nav>
    </header>
    <router-view />
  </div>
</template>


<script>
export default {
  title: 'Charlene Mitchell'
}
</script>


<style>
*{
  margin: 0px;
  padding: 0px;
}
#app {
  font-family: Poppins, Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: #FFE5D9;
  
}
header {
  display: flex;
  justify-content: space-between;
  padding: 0px 20px;
  background-color: #D8E2DC;

}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
  text-decoration: none;
}

nav a.router-link-exact-active {
  color: #9D8189;
}
</style>
