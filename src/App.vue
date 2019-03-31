<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link>
      <router-link to="/gallery">Gallery</router-link>
      <router-link to="/about">About</router-link>  
    </div>
    <transition name='fade' mode="out-in">
      <router-view/>
    </transition>
  </div>
</template>

<style lang="css" scoped>
#app {
  display: grid;
}
#nav {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: 10vh;
  background: #1f2825;
  justify-items: center;
}
#nav a{
  display: grid;
  -webkit-box-align: center;
      -ms-flex-align: center;
          align-items: center;
  align-self: center;
  max-height: 6vh;
  padding: 10px 20px;
  text-decoration: none;
  font-family: 'Quicksand', sans-serif;
  font-size: 25px;
  color: #cce5f9;
  -webkit-transition: .5s;
  transition: .5s;
}
#nav a:hover{
  background: #cce5f9;
  color: #3e4f71;
}
.fade-enter-active, .fade-leave-active {
  transition: 1s;
}
.fade-enter, .fade-leave-to {
  transform: translateX(-100%);
  opacity: 0;
}
</style>
