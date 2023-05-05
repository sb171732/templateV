<template>
  <div id="app" style="height: 100%;">
    <!-- <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </nav> -->
    <router-view/>
  </div>
</template>

<style>
#app {
  font-family: Helvetica, sans-serif;
  text-align: center;
  background-color: #eff0f2;
  padding-bottom: 100px;
}
.header1{
  height: 50px;
  background-color: white;
}
.header2{
  height: 100px;
  background-color: white;
}
.header3{
  height: 60px;
  background-color: white;

}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
.content{
  width: 1200px;
  margin: auto;
  font-size: 14px;
  
}
</style>
