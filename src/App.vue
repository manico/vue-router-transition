<template>
  <div id="app">
    <div class="navigation">
      <router-link to="/">Home</router-link>
      <span> | </span>
      <router-link to="/about">About</router-link>
    </div>
    <!-- <transition name="router-transition"
                mode="out-in"
                :appear="true">
      <router-view/>
    </transition> -->
    <transition name="router-transition"
                mode="out-in"
                enter-active-class="animated slideInLeft"
                leave-active-class="animated slideOutRight"
                :appear="true">
      <router-view/>
    </transition>
  </div>
</template>

<style>
@import "https://cdn.jsdelivr.net/npm/animate.css@3.5.2/animate.min.css";

*,
*:before,
*:after {
  box-sizing: border-box;
}

body {
  background: whitesmoke;
  font-family: Arial, Helvetica, sans-serif;
}

html,
body {
  height: 100%;
  overflow-x: hidden;
}

#app {
  position: relative;
  background: white;
  width: 50%;
  height: 50%;
  border-radius: 0.5em;
  margin: 50px auto 0 auto;
  overflow: hidden;
}

.navigation {
  padding: 2em;
}

/* .router-transition-enter-active,
.router-transition-leave-active {
  transition-property: opacity;
  transition-duration: 0.25s;
}

.router-transition-enter-active {
  transition-delay: 0.25s;
}

.router-transition-enter,
.router-transition-leave-active {
  opacity: 0;
} */

/* .page {
  position: absolute;
  width: 100%;
} */
</style>
