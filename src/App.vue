<template>
   <div id="app">
      <Header />
   </div>
</template>

<script>
import Header from './components/header.vue'

export default {
   name: 'App',
   components: {
      Header,
   }
}

</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=BioRhyme:wght@700&family=DM+Sans:wght@400;700&display=swap');

*,
*::before,
*::after {
   box-sizing: border-box;
   padding: 0;
   margin: 0;
}

ul,
ol {
   list-style: none;
}

body {
   min-height: 100vh;
   scroll-behavior: smooth;
   text-rendering: optimizeSpeed;
   margin: 0;
   line-height: 1.5;
}

#app {
   font-family: 'BioRhyme',serif, 'DM Sans', sans-serif ;
   -webkit-font-smoothing: antialiased;
   -moz-osx-font-smoothing: grayscale;
   color: #333;
}

.container {
   margin: 0 auto;
   padding: 0 15px;
   max-width: 1200px;
}




</style>
