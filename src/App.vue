<template>
  <div id="nav">
    <router-link :class ="{active: $route.name === 'Home'}" to="/">Home</router-link> |
    <router-link :class ="{active: $route.name === 'Cart'}" to="/cart">Cart</router-link>
  </div>
  <router-view/>
  this is the footer
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
html, body{
  margin: 0;
  padding: 0;
}
body{
  background-color:#878788;
  display: flex;
  justify-content: center;
  flex-wrap:wrap;
  align-items: center;
}

#nav {
  width: 100%;
  height: 30px;
  background-color: white;
  
  a{
    font-weight: bold;
    color: darkgray;
    text-decoration: none;
    margin: 0 5px;
    font-size: 1.25rem;

    &.active{
      color:#2c3e50;
    }
  }
}
.text-center{
  text-align: center;
}
</style>
