<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
import Vue from 'vue'
import Buefy from 'buefy'

Vue.use(Buefy)

export default {
  name: 'App'
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

// --- Theme configuration ---

// Import Bulma's core
@import "~bulma/sass/utilities/_all";

// Custom colors colors
$primary: #d3ac17;
$primary-invert: findColorInvert($primary);

// datepicker colors
$datepicker-background-color: #2f353c;
$datepicker-header-color: $grey-light;
$datepicker-today-border: solid 1px $primary;
$datepicker-item-color: $grey-light;
$datepicker-item-disabled-color: $grey-dark;
$datepicker-item-selected-background-color: #ffcc0d;

// Setup $colors to use as bulma classes
$colors: (
    "white": ($white, $black),
    "black": ($black, $white),
    "light": ($light, $light-invert),
    "dark": ($dark, $dark-invert),
    "primary": ($primary, $primary-invert),
    "info": ($info, $info-invert),
    "success": ($success, $success-invert),
    "warning": ($warning, $warning-invert),
    "danger": ($danger, $danger-invert),
);

// Links
$link: $primary;
$link-invert: $primary-invert;
$link-focus-border: $primary;

// Import Bulma and Buefy styles
@import "~bulma";
@import "~buefy/src/scss/buefy";
</style>
